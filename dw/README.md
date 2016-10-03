# Format Markdown to-do lists as HTML

Given a ```list.md``` with custom unicode bullets, for example:

```
- Something to do
  ✔ Already done
  ✘ Does not work like that
  - Still to do
```

one can create the HTML version of the list using the script ```mdg``` and the template ```md-template.html``` from this directory, via the command:
```
mdg list.md
```

which will contain CSS class attributes to allow styling of the custom bullets:
```
<ul>
  <li>Something to do
    <ul>
      <li class="chk">Already done</li>
      <li class="crs">Does not work like that</li>
      <li>Still to do</li>
    </ul>
  </li>
</ul>
```

which can for example look like:

![list.png](https://github.com/dw09/kramdown/blob/custom_bullets/dw/list.png)

Generated HTML [is here](https://github.com/dw09/kramdown/blob/custom_bullets/dw/list.html).
