## ng-content(directive):

Any content written in between the component tags in the parent component html (`app.component.html` for example) will be attached to the <ng-content> tag used in the child component.

`app.component.html:`

```html
<app-child> <p>blah</p> </app-child>
```

`child.component.html:`

```html
<div class="container">
    <div class="row">
        <ng-content></ng-content>
    </div>
</div>
```

Now the paragraph in the app component is attached to the ng-content tag of the child component.
