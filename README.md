# hb-multipage-site

In this exercise you should separate the user interface from any kind of business logic. For this you can use separate modules that are connected using dependencies (`import` and `export`).

Take into consideration the following global rules for all components:
- Each component should have it's one folder.
- Each component should use the [pug-loader](https://github.com/pugjs/pug-loader) to read the template and generate HTML.
- Each component should be implemented using the mobile first approach.
- Each component should be responsive using the following viewports:
  - Small: 0 - 639px
  - Medium: 640px - 1023px
  - Large: 1024 - ∞

## Component

### Main Menu
This component should be present on every page since it is a global component that helps the user to navigate between different pages.

#### Data Structure
```
{
  logo: {
    img: '',
    link: ''
  },
  links: [
    {
      label: ''
      href: '',
    },
    {
      label: ''
      links: [
        {
          label: ''
          href: '',
        }
      ],
    }
  ]
}
```

#### User Interactions
- Hamburguer Icon (Small and Medium):
  - Clicking should display or hide the menu depending on the current state.
- Main Logo:
  - Clicking the main logo should redirect the user to the provided URL.
- Links:
  - Clicking a link should:
    - Follow the provided link, if the link doesn't have a second level of links.
    - Display the second level of links if they were provided.
  - Hovering on a link should change it's visible state.

