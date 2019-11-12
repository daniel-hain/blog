  
 Demote headings (H1 → H2, etc.)
 HTML headings/IDs
 Wrap HTML
Help: Docs, Bugs
<!----- Conversion time: 0.65 seconds.


Using this Markdown file:

1. Cut and paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β17
* Tue Nov 12 2019 04:30:02 GMT-0800 (PST)
* Source doc: https://docs.google.com/open?id=1F7OKPkwEMN_Ntwd659ne2d8qtKXcfCPUdA5VIQ9XePY
----->



# Trump vs. GPT-2


### SDS 2019 - Module 3: Individual Assignment

Deadline: 18/11 - 2019

The site [https://faketrump.ai/](https://faketrump.ai/) is an interesting example of AI-powered fake-text generation. They write:


    _We built an artificial intelligence model by fine-tuning [GPT-2](https://openai.com/blog/better-language-models/) to generate tweets in the style of Donald Trump’s Twitter account. After seeing the results, we also built a discriminator that can accurately detect fake tweets 77% of the time — think you can beat our classifier? Try it yourself!_

GPT-2 is a neural transformer-based model, that has been announced by OpenAI in February 2019 and created considerable discussion because they decided - in contrast to their earlier policies - not to release the mode to the public. Their central argument was that the model could be used to produce fake news, spam and alike too easily. The footnote of the faketrump page reads: “Generating realistic fake text has become much more accessible. We hope to highlight the current state of text generation to demonstrate how difficult it is to discern fiction from reality.”

Since then several organizations and researchers have shown that it is [possible to develop systems to detect “fake text”](https://www.theguardian.com/technology/2019/jul/04/ai-fake-text-gpt-2-concerns-false-information). We believe that you too can implement a competitive system.

This assignment is not about Natural Language Processing (NLP) but about being able to deal with sequential data using deep learning. Some basic knowledge from M2 can be useful to squeeze the last 1% performance but you should be able to get great results with pure Keras. The data can be found [here](https://github.com/DeepLearnI/trump_tweet_classifier/raw/master/code/tweet_labels.csv) and has the following format:


<table>
  <tr>
   <td>tweet
   </td>
   <td>labels
   </td>
  </tr>
  <tr>
   <td>string
   </td>
   <td>boolean
   </td>
  </tr>
</table>


There are 8000 real Trump tweet sand 7348 fake ones.

Having been with us for M2, you may ask: How do I go from text to numerical values that I can use in a neural model?

You can for instance just use the “Tokenizer” that’s part of Keras. 

vocabulary_size = 5000

tokenizer = Tokenizer(num_words= vocabulary_size)

tokenizer.fit_on_texts(df['text'])

sequences = tokenizer.texts_to_sequences(df['text'])

From here, you just need to “pad” the sequences (for en easier workflow).

But what kind of network do you expect me to build?

That’s up to you. Just make sure it is more advanced than a basic feed-forward-net.

Not acceptable solution: You use SpaCy or similar to get average vectors for the tweets and then build an M1 style classifier just using a neural model rather than a random forest or similar.

If you want to build such a simple model as a baseline - that’s fine, but we do expect that you come up with something more advanced.



*   You can use CNNs, RNNs (GRU, LSTM, BiLSTMS), Embedding layers in combinations that you think are useful (explain your choices). 
*   If you want, you are welcome to use pre-trained word-vectors (public domain or homemade). 
*   You can go even deeper and explore transformer-based models, attention and the more recent 2018-19 stuff. 
*   BUT: A top-performance can be achieved just using Keras and no fancy NLP stuff. Be creative and use the 100s of tutorials and recipes on the web.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">A useful abbreviation. <a href="https://t.co/uGywwvaBE6">pic.twitter.com/uGywwvaBE6</a></p>&mdash; Robin Houston (@robinhouston) <a href="https://twitter.com/robinhouston/status/1193105748374491136?ref_src=twsrc%5Etfw">November 9, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


### Deliverables

Please submit a PDF or HTML version of your notebook on peergrade.io (if you submit HTML, please zip it before - large embedded HTMLs from cause crashing when opened directly in peergrade). In addition, include a link to a functioning google Colab notebook or Kaggle kernel (mandatory). Please make sure it runs without errors and others can access it (i.e. own test in “anonymous” setting in your browser).

This notebook should:



*   solve the questions in a straightforward and elegant way.
*   contain enough explanations to enable your fellow students (or others on a similar level of knowledge) to clearly understand what you are doing, why, what is the outcome, how to interpret it, and how to reconstruct the exercise. Be specific and understandable, but brief.

### 
Further process and dates

*   You will receive an upload link on peergrade.io by 15.11 
*   The notebook upload is due 18/11; 23.50. Delays are not accepted.
*   After the upload deadline, you will receive an invitation to peergrade your fellows' exams on peergrade.io. You will be asked for the evaluation of 3 peer-assignments is part of the assignment and mandatory.
*   The peergrade evaluation is due 21/11. Reviewing is part of your performance. Don’t forget that.

<!-- Docs to Markdown version 1.0β17 -->

