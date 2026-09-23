# Phase 5 – Project Development
## UI Policy – High Impact Control
Table: Incident
Active: True
Condition: Impact is 1 – High
Reverse if false: True

### Assignment Group Action
Mandatory: True

### Urgency Action
Read-only: True

## onChange Client Script
Name: Auto set urgency for high impact
Type: onChange
Field: Impact

```javascript
function onChange(control, oldValue, newValue, isLoading) {
    if (isLoading || newValue == '') {
        return;
    }

    if (newValue == '1') {
        g_form.setValue('urgency', '1');
        g_form.addInfoMessage('Urgency set to High for High impact incident.');
    }
}
```

## onSubmit Client Script
Name: Prevent save if Assigned To missing
Type: onSubmit

```javascript
function onSubmit() {
    if (g_form.getValue('impact') == '1' &&
        g_form.getValue('assigned_to') == '') {

        g_form.showErrorBox(
            'assigned_to',
            'Assigned To is mandatory for High impact incidents.'
        );
        return false;
    }
    return true;
}
```

## onCellEdit Client Script
Name: Prevent state change via list edit
Type: onCellEdit
Field: State

```javascript
function onCellEdit(sysIDs, table, oldValues, newValue, callback) {
    alert('State cannot be updated using list editing. Please open the Incident.');
    callback(false);
}
```

## Evidence to Add
Upload screenshots of all three Client Scripts, the UI Policy, and both UI Policy Actions.

### Screenshots

- [High Impact Control UI Policy](./01_High_Impact_Control_UI_Policy.png.jpeg)
- [Auto Set Urgency Client Script](./02_Auto_Set_Urgency_Client_Script.png.jpeg)
- [Prevent Save Assigned To Client Script](./03_Prevent_Save_Assigned_To_Client_Script.png.jpeg)
- [Prevent State Change List Edit](./04_Prevent_State_Change_List_Edit.png.jpeg)
- [Assignment Group UI Policy Action](./05-assignment-group-action.png.jpeg)
- [Urgency UI Policy Action](./06-urgency-action.png.jpeg)
