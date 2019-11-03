---
title: "My First Post"
date: 2019-10-22T16:52:36+02:00
draft: false
js: /js/juniper.min.js

---
stuff


<pre data-executable>
print('This is a demo of Juniper.')
text1 = "It's a JS library for running code in your "
text2 = "browser, via Jupyter kernels provided by {}."
print(text1 + text2.format('Binder'))
</pre>

<pre data-executable data-theme="monokai">
# it starts a Docker container from a pre-built image
# so you can pre-install any libraries
import spacy

nlp = spacy.load('en_core_web_sm')  # spaCy models!
doc = nlp(u"This is a sentence.")
for token in doc:
    print(token.text, token.pos_)
</pre>
