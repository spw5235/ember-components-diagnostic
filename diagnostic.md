# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
   One example could be a blog.

   - post
     - title
     - body
     - comments
       - comments title
       - comments body

   Each part can be broken into components for data up and action down.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    When generating a component, you have a template hbs file created and a model hook is populated in the routes file.  The hbs file is used to create a view-state.  The route defines how to retrieve data.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    <ul>
    {{#each contacts.my-contact as |my-contact|}}
      {{contacts/my-contact my-contact=my-contact}}
    {{/each}}
  </ul>
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    <li>{{my-contact.my-phone}}</li>
    ```
