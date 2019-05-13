Documentation


## Get the Component

`$ git submodule add https://github.com/theNewDynamic/hugo-component-tnd-forms.git components/tnd-forms`

Modify Config `config.yaml`

```
themesDir: components
theme:
- example
- tnd-forms
```

## Creating Forms Locally 

You can add forms directly from your project's `data/forms/` directory. See `data/forms/contact-default.yaml` as an example. 

The filename is used to identify the form.


## Creating Forms from Forestry 

### Add to Forestry

Copy the `front_matter` and `snippets` folders from the `components/tnd-forms/forestry/front_matter` directory to your local project's Forestry folder.

Add Forms to Sidebar (see attached image)

![Forestry](/docs/ScreenShot-forestry-setup-2019-05-13.jpg)


### Add the form in the control panel

Note the name of the form you create as you will use this in the next step:


## Include the Form in an entry:

Forms are including using the `form` shortcode.
To include `data/forms/contact.yaml`:

```markdown
## Contact Us!
{{< form "contact" >}}
```

## Styling

Classes can be added to each form elements using the components' reserved parameter key in your site's configuration file.

_Warning_: If using PurgeCSS, you might have to whitelist classes mentioned in there.

```yaml
params:
  tnd_forms:
    css:
      form: 'max-w-md pb-5'
      control: ''
      required: ''
      submit: block w-full bg-grey hover:bg-grey-darker text-white font-bold py-3 px-4 focus:outline-none focus:shadow-outline
      input: block w-full bg-white text-grey-darker border border-grey py-3 px-4 mb-3 leading-tight focus:outline-none
      textarea: block w-full bg-white text-grey-darker border border-grey py-3 px-4 mb-3 leading-tight focus:outline-none h-48
      label: block uppercase tracking-wide text-grey-darker text-xs font-bold mb-2
      select: block appearance-none w-full rounded-none w-full bg-white text-grey-darker border border-grey py-3 px-4 leading-tight focus:outline-none focus:outline-none focus:shadow-outline
      select_wrapper: inline-block relative w-full mb-3
      select_fake: pointer-events-none absolute pin-y pin-r flex items-center px-2 text-grey-darker
```
