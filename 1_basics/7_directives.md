## Directive example:
```html
<p appTurnGreen>Receives a green background</p>
```

```ts
@Directive({
    selector: '[appTurnGreen]' //attribute notation
})

export class TurnGreenDirective {…}
```

> **_*ngIf_**: * acts as a notation for  structural directive which changes the structure of dom.

### ngIf-else example:

```html
<p *ngIf="serverCreated; else noserver">Server created</p>
<ng-template #noserver>
    <p> server not created </p>
</ng-template>
```
> **_[ngStyle]_** here [] are used since it is not a structural directive.

### ngStyle and ngClass Example:

```html
<p [ngStyle]="{background: someVariable/functionCall/itinerary expression}" [ngClass]="{className: Boolean}"></p>
```

In the above example boolean of ngClass can either be a function call that returns a boolean or an expression that outputs a boolean or a variable of type boolean.

> ngFor is a structural directive so we use *. you can fetch index of the iteration as shown in the below example.

### ngFor Example:

```html
<app-component *ngFor="let element of array; let i = index"></app-component>
```
