---
title: "My First Post"
date: 2019-10-22T16:52:36+02:00
draft: false
js: js/juniper.min.js
css: https://codemirror.net/theme/monokai.css
---

<pre data-executable data-theme="monokai">
# it starts a Docker container from a pre-built image
# so you can pre-install any libraries
import spacy

nlp = spacy.load('en_core_web_sm')  # spaCy models!
doc = nlp(u"This is a sentence.")
for token in doc:
    print(token.text, token.pos_)
</pre>

<script src="js/juniper.min.js"></script>
<script>
    new Juniper({
    repo: 'ines/spacy-io-binder'
    });
    // listen to status updates
    document.addEventListener('juniper', ev =>
    console.log('Status:', ev.detail.status))
</script>