**Massimo** includes a few built-in helpers for convience, but mostly relies on including the helpers from&nbsp;[Padrino::Helpers](http://github.com/padrino/padrino-framework).

Built-in Helpers
----------------

### `site()`

Returns a reference to the current site.

### `config()`

Returns a reference to the current site&rsquo;s configuration.

### `render(view, locals = {})`

Renders a view with the given locals. Kind of like `render :partial` in Rails.


Included Helpers
----------------

 **Massimo** includes all of the modules except the `Padrino::Helpers::RenderHelper`. So check out their [documentation](http://www.padrinorb.com/api/index.html) for more information.