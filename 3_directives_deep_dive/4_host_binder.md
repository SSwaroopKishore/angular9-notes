This decorator can be used to handle any properties of the element that this directive has been bound to.

```ts
@Directive({
    selector: '[appTurnGreen]' //attribute notation and camel case
})
export class TurnGreenDirective implements OnInit{
    @HostBinder('style.backgrounColor') background: string = 'transparent';
    constructor(private elementRef: ElementRef, private renderer: Renderer2) {}
    ngOnInit() {}
    @HostListener('mouseenter') mouseover(eventData: Event) {
        this.background = 'blue';
    }
        
    @HostListener('mouseleave') mouseleave(eventData: Event) {
        this.background = 'transparent';
    }
}
```

> the parameter of the hostBinder is a property of the element.
