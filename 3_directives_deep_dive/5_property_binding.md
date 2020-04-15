```ts
@Directive({
    selector: '[appTurnGreen]' //attribute notation and camel case
})
export class TurnGreenDirective implements OnInit{
    @Input() defaultColor: string = 'transparent';
    @Input('appTurnGreen') highlightColor: string = 'blue';
    @HostBinder('style.backgrounColor') background: string;
    constructor(private elementRef: ElementRef, private renderer: Renderer2) {}
    ngOnInit() {}
    @HostListener('mouseenter') mouseover(eventData: Event) {
        this.background = this.highlightColor;
    }
        
    @HostListener('mouseleave') mouseleave(eventData: Event) {
        this.background = this.defaultColor;
    }
}
```

`HTML:`
```html
<p appTurnGreen [defaultColor]="'yellow'" [highlightColor]="red"></p>
```

If we use alias in `@Input` which is the same name as directive then in HTML we can use it as

```html
<p [appTurnGreen]="'red'" [defaultColor]="'yellow'"></p>
```
or 
```html
<p [appTurnGreen]="'red'" defaultColor="yellow"></p> <!-- but be careful with this notation. -->
```
