---
hide:
  - navigation
  - toc
title: Home
---

<script>
  var models = [
      'https://www.optwiki.site/model-lasso',
      'https://www.optwiki.site/model-lasso'
  ];

  function randomModel() {
      var i = parseInt(Math.random() * models.length);
      location.href = models[i];
  }
</script>

<center>
  
#  Optwiki

:material-pen: _The Optimizer's Reference_

## Our Mission

To create a canonical reference for optimization models and algorithms

[Random Algorithm](<script> randomModel() </script>){ .md-button .md-button--primary }
[Random Model](<a href="#" onclick="randomModel();"></a>){ .md-button .md-button--primary }

## How it Works

- Anyone can submit edits / additions via Github.[^1]
- [Github issues](https://github.com/OptWiki/site/issues) are used to faciliate content discussion.

[^1]: Note the pencil "edit" button on each page.

<br>

[Contact Us](https://form.jotform.com/heatonforms/contact){ .md-button .md-button--primary }
  
<a href="#" onclick="randomModel();">Random Model</a>
</center>
