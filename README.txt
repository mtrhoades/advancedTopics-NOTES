Module 1:

*Sassy Cascading Style Sheets* (SCSS)

CSS vs. SCSS
    ^ CSS has no logic or functions, where as SCSS does.

Sass (package compiler) / SCSS (Sass CSS) --->
    like other CSS preprocessors are translated to CSS, this process is called compiling.

    Basic features:
        •Variables (Note: Different than CSS variables)
        •Nesting
        •Partials
        •Functions and Mixins
        •Extend and Placeholder Selectors

    variables - prefixed $ notation
        variable naming - kebab-case naming convention from CSS

           * During compiling, the variable names will be replaced with their values.

    Advanced features:
        loops

        if Directive

        interpolation

        Data Types

        nesting --->
            SCSS:
                .parent{
                    .child{}
                }

            Compiled into CSS:
                .parent .child{}

        * The ampersand (&) is a special parent selector in SCSS. It always refers to the outer selector. It's like a placeholder.

        Sass documentation discourages nesting selectors too deeply.
            •Difficult to visualize how much CSS is being generated
            •Taxing to serve
            •Taxing for the browser
            * Keep your nested selectors shallow!


- CSS variables (vars) can be accessed through javascript, but SCSS variables cannot be accessed through javascript since they are compiled into CSS for the browser to run it.

    At-Rules --->

        @mixin - Essentially, a @mixin is a directive that allows us to group and reuse rules.
            This is the basic structure of the @mixin:
                •First, use the @mixin directive.
                •The name will follow.
                •The encapsulated rules are then wrapped in curly braces.

                    @mixin name {
                        property: value;
                        property: value;
                        ...
                    }

        @include - Next, in order to make use of our handy group of rules (@mixin), we need to @include it.

            The @mixin directive can also accept arguments.
                Note: All @mixin arguments must be denoted with the SassScript $variable syntax.

                    @mixin bordered($color, $type) {
                        color: @color;
                        border-style: $type;
                        width: 50px;
                    }
                    .box {
                        @include bordered(#77C1EF, solid);
                    }

            * Just like JavaScript functions, the @mixin directive accepts optional or default arguments.

                @mixin bordered($color: black, $type: dotted) {
                        color: @color;
                        border-style: $type;
                        width: 50px;
                    }

        @content - The @content directive allows the @mixin to expect and accept additional content.
            Whatever is passed within the curly braces will replace @content during the compilation process.

        @import - imports other code (modules)


****************************************************************************************************************************
Module 2: (Sass)

advanced At-Rules and flow control --->
    


*****************************************************************************************************************************
Module 3:

TypeScript Basics --->


****************************************************************************************************************************
Module 4: 

Generics and Asynchronous TypeScript --->
    