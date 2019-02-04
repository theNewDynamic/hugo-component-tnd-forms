# TND Forms

Hugo components for handling forms.

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
