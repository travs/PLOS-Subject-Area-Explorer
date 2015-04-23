# PLOS-Subject-Area-Explorer
Embeddable tree picker of PLOS thesaurus terms

##Usage

[Install bootstrap-treeview](https://github.com/jonmiles/bootstrap-treeview#install) (`bower install bootstrap-treeview`).

Insert something like this into your document

```
<div id="tree"></div>
```

Now create the treeview with PLOS subject area data:

```
$.getJSON('https://rawgit.com/travs/PLOS-Subject-Area-Explorer/master/thesaurus_latest.json', function(data){
  $('#tree').treeview({data: data});
})
```

##Attributions

This uses data that I converted to JSON to be compatible with bootstrap-treeview.

The data comes from PLOS, and is hosted [over here](https://github.com/PLOS/plos-thesaurus).
