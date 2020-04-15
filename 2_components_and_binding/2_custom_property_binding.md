For an example consider that we have a parent component `app-component` and a child component `app-server-component`.

`app.component.html:`

```html
<app-server-component *ngFor="let serverElement of serverElements" [srvElement]="serverElement"></app-server-component>
```

`server.component.ts:`

```ts
export class serverComponet implements OnInit {
    @Input('srvElement') element : {type: string, name: string, content: string};
    constructor(){}
    ngOnInit(){}
}
```

> `@Input` used above will act as an enabler of super import where the element property of serverComponent can be used by it's parent appComponent using the alias srvElement. Here `@Input` indicates that some information is being shared to the component from the parent component.
