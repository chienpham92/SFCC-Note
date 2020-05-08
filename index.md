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
[templateDebugger.ds](/debug/templateDebugger.ds)
