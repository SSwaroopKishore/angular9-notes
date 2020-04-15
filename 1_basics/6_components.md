You can generate components using ng cli or by manually creating a typescript class and annotating it with at the @component decorator.

The properties of component decorator are:

* **_selector_**: This selector will be used by us to inject this particular component wherever required. You can use the selector to be of type element, attribute, class. The notations are respectively as follows
    * selector: 'app-server'
    * selector: '[app-server]'
    * selector: '.app-server'

* **_template_**: You can use it to directly write your template of the component in this file. You can use single line or multiline templates
    * ```html
        <div class="blah"></div>
        ```
    * ```html
        <div class="big blah">
            <div class="small blah"></div>
        </div>
        ```

* **_templateUrl_**: URL of the template for the component.

* **_styles_**: Same as template you can either use single line or multiline Styles directly written in the component files using this property.

* **_styleUrls_**: Takes an array of paths of style sheets that are meant for this component.
