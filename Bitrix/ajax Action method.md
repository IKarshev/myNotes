```js
BX.ajax.runComponentAction('IK:form', 'Send_Form', {
    mode: 'class',
    data: new FormData(document.getElementById(`${form_id}`)),
}).then(
    response => {

    },
    error => {

    }
);
```
