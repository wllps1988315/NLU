How do you train a sequence tagger in BIO scheme?  <br>
A.Optimise cross-entropy for every time step.  <br>
B.Optimise accuracy for every time step.  <br>
C.Optimise accuracy for the whole sequence.  <br>

答案：A

 
 
 
 Slot tagger <br>
 --What you can do:  <br>
    ~Handcrafted rules like regular expressions  <br>
    ~CRF   <br>
    ~RNN seq2seq  <br>
    ~Any seq2seq with attention  <br>
    

Can you replace non-symmetric convolutional kernel (blue triangle) with symmetric kernel (taking both left and right neighbours) in <br>
this architecture for language modeling? <br>

![](./pic/cnn.jpeg)

<br>
A.Yes  <br>
B.No   <br>
答案：B

Let's add lexicon features to input words <br>
~Let's match every n-grame of input text against entries in our lexicon <br>
![](./pic/lexicon.jpeg)

<br>
~A match is successful when the n-gram matches the prefix or postfix of an entry and is at least half the length of the entry <br>
Matches:  <br>
"San"--->"San Antonio"  <br>
"San"--->"San Francisco"  <br>
"San Francisco"--->"San Francisco"  <br>

When there are multiple overlapping matches: <br>
~Prefer exact matches over partial  <br>
~Prefer longer matches over shorter  <br>
~Prefer earlier matches in the sentence over later <br>

![](./pic/BIEO_encoding_algorithm.jpeg) 
<br>
![](./pic/BIEO_encoding_algorithm1.jpeg) 
<br>