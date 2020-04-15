Consider this example:

```html
<input type="text" [(ngModel)]="serverName">
<button (click)="onServerAdded()">add</button>
```

The above line can be replace by

```html
<input type="text" #serverNameInput>
<button (click)="onServerAdded(serverNameInput)">add</button>
```

In the second example `serverNameInput` is not going to be the value of the input field but the whole input element itself. So we need to extract the value of the filed using the element properties as follows:

```js
{
    name: serverNameInput.value,
    ...,
}
```

`@ViewChild` can also be used instead of passing the `serverNameInput`  in the click event.

`html:`
```html
<input type="text" #serverNameInput>
```
`ts:`
```ts
@ViewChild('serverNameInput') serverNameInputRef : ElementRef;
........;
{
    name: serverNameInputRef.nativeElement.value,
    ....,
}
```

> Need to observe that in the last example `@ViewChild` is receiving an `ElementRef` type and not the `Element` type.
