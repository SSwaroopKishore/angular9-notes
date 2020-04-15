```ts
@Directive({
    selector: '[appTurnGreen]' //attribute notation and camel case
})
export class TurnGreenDirective implements OnInit{
    constructor(private elementRef: ElementRef, private renderer: Renderer2) {}
    ngOnInit() {
        this.renderer.setStyle(this.elementRef.nativeElement, 'background-color', 'transparent', '!important');
    }
        
    @HostListener('mouseenter') mouseover(eventData: Event) {
        this.renderer.setStyle(this.elementRef.nativeElement, 'background-color', 'blue', '!important');
    }
        
    @HostListener('mouseleave') mouseleave(eventData: Event) {
        this.renderer.setStyle(this.elementRef.nativeElement, 'background-color', 'transparent', '!important');
    }
        
}
```

In the above example if we hover on the element with this directive the background color changes to blue and if not the color changes back to transparent or body color. 

> So `@HostListener` can be used to make the directive listen to user events.Parameters of hostListener are actual `user events`.
