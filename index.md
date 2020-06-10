## Welcome to GitHub Pages
[View guide syntax](https://chienpham92.github.io/SFCC-Note/guide)

You can use the [editor on GitHub](https://github.com/chienpham92/SFCC-Note/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

##Views

### Basic print value
`${pdict.name}`
###  Pipeline Dictionary to Global Variable
pdict	keys - Alternatives <br/>
```javascript 
 session, request, customer, request.httpParameterMap, request.pageMetaData, session.forms
```
### print value in script tag

    <script>
         function test() {
            return {
                'name': <isprint value="${JSON.stringify(pdict.name)}" encoding="off"/>
            }
        }
    </script>

### Debug isml variable 
![step 1](/debug/debug_isml.png)
![step 2](/debug/debug_isml_result.png)
[TemplateDebugger.ds](/debug/TemplateDebugger.ds)

### JQuery in ISML Templates
Avoid using the # character in jQuery or JavaScript because it's reserved in ISML templates and can cause problems.

Instead of use: 

```html
<a id="id-to-select" href="#">Link</a>
<script>
    jQuery("#id-to-select").click(function() {
        // Code here
    });
</script>
```
Use the following code:
```html
<a id="id-to-select" href="${'#'}">Link</a>
<script type="text/javascript">
    jQuery("a[id='id-to-select']").click(function() {
        // Code here
    });
</script>
```