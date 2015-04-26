# PLOS-Subject-Area-Explorer
Embeddable tree picker of PLOS thesaurus terms

##Usage

[Install bootstrap-treeview](https://github.com/jonmiles/bootstrap-treeview#install) (`bower install bootstrap-treeview`).

Insert something like this into your document

```html
<div id="tree"></div>
```

Now create the treeview with the *latest* PLOS subject area data:

```js
var sha = jQuery.ajax({url: 'https://api.github.com/repos/travs/PLOS-Subject-Area-Explorer/commits', success: function(data){
var sha = data[0].sha;
var URL = 'https://cdn.rawgit.com/travs/PLOS-Subject-Area-Explorer/' + sha + '/thesaurus_latest.min.json'
$.getJSON(URL, function(data){
  $('#tree').treeview({data: data, levels: 1, nodeIcon: 'glyphicon'});
})}})
```

Insert the above into a `<script>` element at the bottom of your page if you like, or in another script file.

##Attributions

This uses data that I converted to JSON to be compatible with bootstrap-treeview.

The data comes from PLOS, and is hosted [over here](https://github.com/PLOS/plos-thesaurus).
