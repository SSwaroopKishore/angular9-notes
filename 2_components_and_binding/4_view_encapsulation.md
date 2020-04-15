Angular enforces the styles added in the css files specific to a component to be applied only to the elements of that component and not to any other parent or sibling components.

> to change this config we can use the encapsulation property of the @component decorator.

`Example:`

```ts
@Component({
    selector: ...,
    styles: ...,
    templateUrl: ...,
    encapsulation: ViewEncapsulation.Emulated //(default) None and Native are other properties
})
```