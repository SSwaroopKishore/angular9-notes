For an example consider that we have a parent component `app-component` and a child component `app-server-component`.

`app.component.html:`

```html
<app-server-component (svcCreated)="onServerAdded($event)"></app-server-component>
```

`app.component.ts:`

```ts
onServerAdded(serverData: {name: string, content: string}) {
    this.servers.push({
        name: serverData.name,
        content: serverData.content
    });
}
```
                        
`server.component.ts:`

```ts
export class serverComponet implements OnInit {
    @Output('svcCreated') serverCreated : EventEmitter<{name:string,content:string}> = new EventEmitter();
    constructor(){}
    ngOnInit(){}
    onServerCreated() { //click event inputting values from textboxes
        this.serverCreated.emit({
            name: this.name,
            content: this.content
        })
    }
}
```
