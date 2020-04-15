```html
<div *ngIf="!onlyOdd">
    <li class="list-group-item" *ngFor="let even of evenNumbers">
        {{even}}
    </li>
</div>
```

above code is equivalent to:

```html
<ng-template [ngIf]="!onlyOdd">
    <div>
        <li class="list-group-item" *ngFor="let even of evenNumbers">
            {{even}}
        </li>
    </div>
</ng-template>
```