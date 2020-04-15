## Decorators and config options:

`TS file:`

```ts
@Directive({
    selector: '[appTurnGreen]' //attribute notation and camel case
})
export class TurnGreenDirective implements OnInit{
    constructor(private elementRef: ElementRef) {}
    ngOnInit() {
        this.elementRef.nativeElement.style.background = 'green'
    }
}
```

`Html file:`

```html
<p appTurnGreen>appTurnGreen will turn my background to green</p>
```
>* Use camelcase for selector of directives.
>* constructor of a directive has params by default which are ElementRef or Renderer2.
>* It is advised to use renderer because for dom manipulations because the dom might not always be available to use ElementRef so in that case we use renderer by angular.

`Example for rendere2:`

```ts

@Directive({
    selector: '[appTurnGreen]' //attribute notation and camel case
})
export class TurnGreenDirective implements OnInit{
    constructor(private elementRef: ElementRef, private renderer: Renderer2) {}
    ngOnInit() {
        this.renderer.setStyle(this.elementRef.nativeElement, 'background-color', 'blue', '!important');
    }
}
```
