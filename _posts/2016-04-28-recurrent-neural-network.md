---
layout: page
title: "Recurrent Neural Network"
category: nn
---
<h2>
<a id="table-of-contents" class="anchor" href="#table-of-contents" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Table of Contents</h2>

<ul>
<li><a href="#codes">Codes</a></li>
<li>
<a href="#theory">Theory</a>

<ul>
<li><a href="#lectures">Lectures</a></li>
<li><a href="#books--thesis">Books / Thesis</a></li>
<li><a href="#network-variants">Network Variants</a></li>
<li><a href="#surveys">Surveys</a></li>
</ul>
</li>
<li>
<a href="#applications">Applications</a>

<ul>
<li><a href="#language-modeling">Language Modeling</a></li>
<li><a href="#speech-recognition">Speech Recognition</a></li>
<li><a href="#machine-translation">Machine Translation</a></li>
<li><a href="#conversation-modeling">Conversation Modeling</a></li>
<li><a href="#image-captioning">Image Captioning</a></li>
<li><a href="#video-captioning">Video Captioning</a></li>
<li><a href="#question-answering">Question Answering</a></li>
<li><a href="#image-generation">Image Generation</a></li>
<li><a href="#turing-machines">Turing Machines</a></li>
<li><a href="#robotics">Robotics</a></li>
<li><a href="#other">Other</a></li>
</ul>
</li>
<li><a href="#datasets">Datasets</a></li>
<li><a href="#blogs">Blogs</a></li>
<li><a href="#online-demos">Online Demos</a></li>
</ul>

<h2>
<a id="codes" class="anchor" href="#codes" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Codes</h2>

<ul>
<li>
<a href="https://www.tensorflow.org/">Tensorflow</a> - Python, C++

<ul>
<li>
<a href="https://www.tensorflow.org/versions/master/get_started/index.html">Get started</a>, <a href="https://www.tensorflow.org/versions/master/tutorials/index.html">Tutorials</a>

<ul>
<li><a href="https://www.tensorflow.org/versions/master/tutorials/recurrent/index.html">Recurrent Neural Network Tutorial</a></li>
<li><a href="https://www.tensorflow.org/versions/master/tutorials/seq2seq/index.html">Sequence-to-Sequence Model Tutorial</a></li>
</ul>
</li>
<li>
<a href="https://github.com/nlintz/TensorFlow-Tutorials">Tutorials</a> by nlintz</li>
<li>
<a href="https://github.com/aymericdamien/TensorFlow-Examples">Notebook examples</a> by aymericdamien</li>
<li>
<a href="https://github.com/tensorflow/skflow">Scikit Flow (skflow)</a> - Simiplied Scikit-learn like Interface for TensorFlow</li>
<li>
<a href="http://keras.io/">Keras</a> : (Tensorflow / Theano)-based modular deep learning library similar to Torch</li>
<li>
<a href="https://github.com/sherjilozair/char-rnn-tensorflow">char-rnn-tensorflow</a> by sherjilozair: char-rnn in tensorflow</li>
</ul>
</li>
<li>
<a href="http://deeplearning.net/software/theano/">Theano</a> - Python

<ul>
<li>Simple IPython <a href="http://nbviewer.ipython.org/github/craffel/theano-tutorial/blob/master/Theano%20Tutorial.ipynb">tutorial on Theano</a>
</li>
<li>
<a href="http://www.deeplearning.net/tutorial/">Deep Learning Tutorials</a>

<ul>
<li><a href="http://www.deeplearning.net/tutorial/rnnslu.html#rnnslu">RNN for semantic parsing of speech</a></li>
<li><a href="http://www.deeplearning.net/tutorial/lstm.html#lstm">LSTM network for sentiment analysis</a></li>
</ul>
</li>
<li>
<a href="http://deeplearning.net/software/pylearn2/">Pylearn2</a> : Library that wraps a lot of models and training algorithms in deep learning</li>
<li>
<a href="https://github.com/mila-udem/blocks">Blocks</a> : modular framework that enables building neural network models</li>
<li>
<a href="http://keras.io/">Keras</a> : (Tensorflow / Theano)-based modular deep learning library similar to Torch</li>
<li>
<a href="https://github.com/Lasagne/Lasagne">Lasagne</a> : Lightweight library to build and train neural networks in Theano</li>
<li>
<a href="https://github.com/gwtaylor/theano-rnn">theano-rnn</a> by Graham Taylor</li>
<li>
<a href="https://github.com/IndicoDataSolutions/Passage">Passage</a> : Library for text analysis with RNNs</li>
<li>
<a href="https://github.com/Ivaylo-Popov/Theano-Lights">Theano-Lights</a> : Contains many generative models</li>
</ul>
</li>
<li>
<a href="https://github.com/BVLC/caffe">Caffe</a> - C++ with MATLAB/Python wrappers

<ul>
<li>
<a href="http://jeffdonahue.com/lrcn/">LRCN</a> by Jeff Donahue</li>
</ul>
</li>
<li>
<a href="http://torch.ch/">Torch</a> - Lua

<ul>
<li>
<a href="https://github.com/karpathy/char-rnn">char-rnn</a> by Andrej Karpathy : multi-layer RNN/LSTM/GRU for training/sampling from character-level language models</li>
<li>
<a href="https://github.com/karpathy/neuraltalk2">neuraltalk2</a> by Andrej Karpathy : Recurrent Neural Network captions image, much faster and better version of the original <a href="https://github.com/karpathy/neuraltalk">neuraltalk</a>
</li>
<li>
<a href="https://github.com/wojzaremba/lstm">LSTM</a> by Wojciech Zaremba : Long Short Term Memory Units to train a language model on word level Penn Tree Bank dataset</li>
<li>
<a href="https://github.com/oxford-cs-ml-2015">Oxford</a> by Nando de Freitas : Oxford Computer Science - Machine Learning 2015 Practicals</li>
<li>
<a href="https://github.com/Element-Research/rnn">rnn</a> by Nicholas Leonard : general library for implementing RNN, LSTM, BRNN and BLSTM (highly unit tested).</li>
</ul>
</li>
<li>
<a href="http://deeplearning4j.org/">DL4J</a> by <a href="http://www.skymind.io/">Skymind</a> : Deep Learning library for Java, Scala &amp; Clojure on Hadoop, Spark &amp; GPUs

<ul>
<li>
<a href="http://deeplearning4j.org/">Documentation</a> (Also in <a href="http://deeplearning4j.org/zh-index.html">Chinese</a>, <a href="http://deeplearning4j.org/ja-index.html">Japanese</a>, <a href="http://deeplearning4j.org/kr-index.html">Korean</a>) : <a href="http://deeplearning4j.org/usingrnns.html">RNN</a>, <a href="http://deeplearning4j.org/lstm.html">LSTM</a>
</li>
<li><a href="https://github.com/deeplearning4j/dl4j-0.4-examples/tree/master/src/main/java/org/deeplearning4j/examples/rnn">rnn examples</a></li>
</ul>
</li>
<li>Etc.

<ul>
<li>
<a href="http://neon.nervanasys.com/docs/latest/index.html">Neon</a>: new deep learning library in Python, with support for RNN/LSTM, and a fast image captioning model</li>
<li>
<a href="https://github.com/IDSIA/brainstorm">Brainstorm</a>: deep learning library in Python, developed by IDSIA, thereby including various recurrent structures</li>
<li>
<a href="http://chainer.org/">Chainer</a> : new, flexible deep learning library in Python</li>
<li>
<a href="http://joschu.github.io/">CGT</a>(Computational Graph Toolkit) : replicates Theano's API, but with very short compilation time and multithreading</li>
<li>
<a href="http://sourceforge.net/p/rnnl/wiki/Home/">RNNLIB</a> by Alex Graves : C++ based LSTM library</li>
<li>
<a href="http://rnnlm.org/">RNNLM</a> by Tomas Mikolov : C++ based simple code</li>
<li>
<a href="https://github.com/yandex/faster-rnnlm">faster-RNNLM</a> of Yandex : C++ based rnnlm implementation aimed to handle huge datasets</li>
<li>
<a href="https://github.com/karpathy/neuraltalk">neuraltalk</a> by Andrej Karpathy : numpy-based RNN/LSTM implementation</li>
<li>
<a href="https://gist.github.com/karpathy/587454dc0146a6ae21fc">gist</a> by Andrej Karpathy : raw numpy code that implements an efficient batched LSTM</li>
<li>
<a href="https://github.com/karpathy/recurrentjs">Recurrentjs</a> by Andrej Karpathy : a beta javascript library for RNN</li>
<li>
<a href="https://github.com/5vision/DARQN">DARQN</a> by 5vision : Deep Attention Recurrent Q-Network</li>
</ul>
</li>
</ul>

<h2>
<a id="theory" class="anchor" href="#theory" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Theory</h2>

<h3>
<a id="lectures" class="anchor" href="#lectures" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Lectures</h3>

<ul>
<li>Stanford NLP (<a href="http://cs224d.stanford.edu/index.html">CS224d</a>) by Richard Socher

<ul>
<li>
<a href="http://cs224d.stanford.edu/lecture_notes/LectureNotes3.pdf">Lecture Note 3</a> : neural network basics</li>
<li>
<a href="http://cs224d.stanford.edu/lecture_notes/LectureNotes4.pdf">Lecture Note 4</a> : RNN language models, bi-directional RNN, GRU, LSTM</li>
</ul>
</li>
<li>Stanford vision (<a href="http://cs231n.github.io/">CS231n</a>) by Andrej Karpathy

<ul>
<li>About NN basic, and CNN</li>
</ul>
</li>
<li>Oxford <a href="https://www.cs.ox.ac.uk/people/nando.defreitas/machinelearning/">Machine Learning</a> by Nando de Freitas

<ul>
<li>
<a href="https://www.youtube.com/watch?v=56TYLaQN4N8">Lecture 12</a> : Recurrent neural networks and LSTMs</li>
<li>
<a href="https://www.youtube.com/watch?v=-yX1SYeDHbg">Lecture 13</a> : (guest lecture) Alex Graves on Hallucination with RNNs</li>
</ul>
</li>
</ul>

<h3>
<a id="books--thesis" class="anchor" href="#books--thesis" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Books / Thesis</h3>

<ul>
<li>Alex Graves (2008)

<ul>
<li><a href="http://www.cs.toronto.edu/%7Egraves/preprint.pdf">Supervised Sequence Labelling with Recurrent Neural Networks</a></li>
</ul>
</li>
<li>Tomas Mikolov (2012)

<ul>
<li><a href="http://www.fit.vutbr.cz/%7Eimikolov/rnnlm/thesis.pdf">Statistical Language Models based on Neural Networks</a></li>
</ul>
</li>
<li>Ilya Sutskever (2013)

<ul>
<li><a href="http://www.cs.utoronto.ca/%7Eilya/pubs/ilya_sutskever_phd_thesis.pdf">Training Recurrent Neural Networks</a></li>
</ul>
</li>
<li>Richard Socher (2014)

<ul>
<li><a href="http://nlp.stanford.edu/%7Esocherr/thesis.pdf">Recursive Deep Learning for Natural Language Processing and Computer Vision</a></li>
</ul>
</li>
</ul>

<h3>
<a id="network-variants" class="anchor" href="#network-variants" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Network Variants</h3>

<ul>
<li>Bi-directional RNN [<a href="http://www.di.ufpe.br/%7Efnj/RNA/bibliografia/BRNN.pdf">Paper</a>]

<ul>
<li>Mike Schuster and Kuldip K. Paliwal, <em>Bidirectional Recurrent Neural Networks</em>, Trans. on Signal Processing 1997</li>
</ul>
</li>
<li>LSTM [<a href="http://deeplearning.cs.cmu.edu/pdfs/Hochreiter97_lstm.pdf">Paper</a>]

<ul>
<li>Sepp Hochreiter and Jurgen Schmidhuber, <em>Long Short-Term Memory</em>, Neural Computation 1997</li>
</ul>
</li>
<li>Multi-dimensional RNN [<a href="http://arxiv.org/pdf/0705.2011.pdf">Paper</a>]

<ul>
<li>Alex Graves, Santiago Fernandez, and Jurgen Schmidhuber, <em>Multi-Dimensional Recurrent Neural Networks</em>, ICANN 2007</li>
</ul>
</li>
<li>GRU (Gated Recurrent Unit) [<a href="http://arxiv.org/pdf/1406.1078.pdf">Paper</a>]

<ul>
<li>Kyunghyun Cho, Bart van Berrienboer, Caglar Gulcehre, Dzmitry Bahdanau, Fethi Bougares, Holger Schwenk, and Yoshua Bengio, <em>Learning Phrase Representations using RNN Encoder-Decoder for Statistical Machine Translation</em>, arXiv:1406.1078 / EMNLP 2014</li>
</ul>
</li>
<li>NTM [<a href="http://arxiv.org/pdf/1410.5401">Paper</a>]

<ul>
<li>A.Graves, G. Wayne, and I. Danihelka., <em>Neural Turing Machines,</em> arXiv preprint arXiv:1410.5401 </li>
</ul>
</li>
<li>Neural GPU [<a href="http://arxiv.org/pdf/1511.08228.pdf">Paper</a>]

<ul>
<li>Łukasz Kaiser, Ilya Sutskever, arXiv:1511.08228 / ICML 2016 (under review)</li>
</ul>
</li>
<li>Memory Network [<a href="http://arxiv.org/pdf/1410.3916">Paper</a>]

<ul>
<li>Jason Weston, Sumit Chopra, Antoine Bordes, <em>Memory Networks,</em> arXiv:1410.3916 </li>
</ul>
</li>
<li>GFRNN [<a href="http://arxiv.org/pdf/1502.02367">Paper-arXiv</a>] [<a href="http://jmlr.org/proceedings/papers/v37/chung15.pdf">Paper-ICML</a>] [<a href="http://jmlr.org/proceedings/papers/v37/chung15-supp.pdf">Supplementary</a>]

<ul>
<li>Junyoung Chung, Caglar Gulcehre, Kyunghyun Cho, Yoshua Bengio, <em>Gated Feedback Recurrent Neural Networks</em>, arXiv:1502.02367 / ICML 2015</li>
</ul>
</li>
<li>Tree-Structured RNNs

<ul>
<li>Kai Sheng Tai, Richard Socher, and Christopher D. Manning, <em>Improved Semantic Representations From Tree-Structured Long Short-Term Memory Networks</em>, arXiv:1503.00075 / ACL 2015 [<a href="http://arxiv.org/pdf/1503.00075">Paper</a>]</li>
<li>Samuel R. Bowman, Christopher D. Manning, and Christopher Potts, <em>Tree-structured composition in neural networks without tree-structured architectures</em>, arXiv:1506.04834 [<a href="http://arxiv.org/pdf/1506.04834">Paper</a>]</li>
</ul>
</li>
<li>Grid LSTM [<a href="http://arxiv.org/pdf/1507.01526">Paper</a>]

<ul>
<li>Nal Kalchbrenner, Ivo Danihelka, and Alex Graves, <em>Grid Long Short-Term Memory</em>, arXiv:1507.01526</li>
</ul>
</li>
<li>Pointer Network [<a href="http://arxiv.org/pdf/1506.03134">Paper</a>]

<ul>
<li>Oriol Vinyals, Meire Fortunato, and Navdeep Jaitly, <em>Pointer Networks</em>, arXiv:1506.03134 / NIPS 2015</li>
</ul>
</li>
<li>Deep Attention Recurrent Q-Network [<a href="http://arxiv.org/abs/1512.01693">Paper</a>]

<ul>
<li>Ivan Sorokin, Alexey Seleznev, Mikhail Pavlov, Aleksandr Fedorov, Anastasiia Ignateva, <em>Deep Attention Recurrent Q-Network</em> , arXiv:1512.01693 </li>
</ul>
</li>
</ul>

<h3>
<a id="surveys" class="anchor" href="#surveys" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Surveys</h3>

<ul>
<li>Yann LeCun, Yoshua Bengio, and Geoffrey Hinton, <a href="http://www.nature.com/nature/journal/v521/n7553/pdf/nature14539.pdf">Deep Learning</a>, Nature 2015</li>
<li>Klaus Greff, Rupesh Kumar Srivastava, Jan Koutnik, Bas R. Steunebrink, Jurgen Schmidhuber, <a href="http://arxiv.org/pdf/1503.04069">LSTM: A Search Space Odyssey</a>, arXiv:1503.04069</li>
<li>Zachary C. Lipton, <a href="http://arxiv.org/pdf/1506.00019">A Critical Review of Recurrent Neural Networks for Sequence Learning</a>, arXiv:1506.00019</li>
<li>Andrej Karpathy, Justin Johnson, Li Fei-Fei, <a href="http://arxiv.org/pdf/1506.02078">Visualizing and Understanding Recurrent Networks</a>, arXiv:1506.02078</li>
<li>Rafal Jozefowicz, Wojciech Zaremba, Ilya Sutskever, <a href="http://jmlr.org/proceedings/papers/v37/jozefowicz15.pdf">An Empirical Exploration of Recurrent Network Architectures</a>, ICML, 2015.</li>
</ul>

<h2>
<a id="applications" class="anchor" href="#applications" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Applications</h2>

<h3>
<a id="language-modeling" class="anchor" href="#language-modeling" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Language Modeling</h3>

<ul>
<li>Tomas Mikolov, Martin Karafiat, Lukas Burget, Jan "Honza" Cernocky, Sanjeev Khudanpur, <em>Recurrent Neural Network based Language Model</em>, Interspeech 2010 [<a href="http://www.fit.vutbr.cz/research/groups/speech/publi/2010/mikolov_interspeech2010_IS100722.pdf">Paper</a>]</li>
<li>Tomas Mikolov, Stefan Kombrink, Lukas Burget, Jan "Honza" Cernocky, Sanjeev Khudanpur, <em>Extensions of Recurrent Neural Network Language Model</em>, ICASSP 2011 [<a href="http://www.fit.vutbr.cz/research/groups/speech/publi/2011/mikolov_icassp2011_5528.pdf">Paper</a>]</li>
<li>Stefan Kombrink, Tomas Mikolov, Martin Karafiat, Lukas Burget, <em>Recurrent Neural Network based Language Modeling in Meeting Recognition</em>, Interspeech 2011 [<a href="http://www.fit.vutbr.cz/%7Eimikolov/rnnlm/ApplicationOfRNNinMeetingRecognition_IS2011.pdf">Paper</a>]</li>
<li>Jiwei Li, Minh-Thang Luong, and Dan Jurafsky, <em>A Hierarchical Neural Autoencoder for Paragraphs and Documents</em>, ACL 2015 [<a href="http://arxiv.org/pdf/1506.01057">Paper</a>], [<a href="https://github.com/jiweil/Hierarchical-Neural-Autoencoder">Code</a>]</li>
<li>Ryan Kiros, Yukun Zhu, Ruslan Salakhutdinov, and Richard S. Zemel, <em>Skip-Thought Vectors</em>, arXiv:1506.06726 / NIPS 2015 [<a href="http://arxiv.org/pdf/1506.06726.pdf">Paper</a>]</li>
<li>Yoon Kim, Yacine Jernite, David Sontag, and Alexander M. Rush, <em>Character-Aware Neural Language Models</em>, arXiv:1508.06615 [<a href="http://arxiv.org/pdf/1508.06615">Paper</a>]</li>
<li>Xingxing Zhang, Liang Lu, and Mirella Lapata, <em>Tree Recurrent Neural Networks with Application to Language Modeling</em>, arXiv:1511.00060 [<a href="http://arxiv.org/pdf/1511.00060.pdf">Paper</a>]</li>
<li>Felix Hill, Antoine Bordes, Sumit Chopra, and Jason Weston, <em>The Goldilocks Principle: Reading children's books with explicit memory representations</em>, arXiv:1511.0230 [<a href="http://arxiv.org/pdf/1511.02301.pdf">Paper</a>] </li>
</ul>

<h3>
<a id="speech-recognition" class="anchor" href="#speech-recognition" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Speech Recognition</h3>

<ul>
<li>Geoffrey Hinton, Li Deng, Dong Yu, George E. Dahl, Abdel-rahman Mohamed, Navdeep Jaitly, Andrew Senior, Vincent Vanhoucke, Patrick Nguyen, Tara N. Sainath, and Brian Kingsbury, <em>Deep Neural Networks for Acoustic Modeling in Speech Recognition</em>, IEEE Signam Processing Magazine 2012 [<a href="http://cs224d.stanford.edu/papers/maas_paper.pdf">Paper</a>]</li>
<li>Alex Graves, Abdel-rahman Mohamed, and Geoffrey Hinton, <em>Speech Recognition with Deep Recurrent Neural Networks</em>, arXiv:1303.5778 / ICASSP 2013 [<a href="http://www.cs.toronto.edu/%7Efritz/absps/RNN13.pdf">Paper</a>]</li>
<li>Jan Chorowski, Dzmitry Bahdanau, Dmitriy Serdyuk, Kyunghyun Cho, and Yoshua Bengio, <em>Attention-Based Models for Speech Recognition</em>, arXiv:1506.07503 / NIPS 2015 [<a href="http://arxiv.org/pdf/1506.07503">Paper</a>]</li>
<li>Haşim Sak, Andrew Senior, Kanishka Rao, and Françoise Beaufays. <em>Fast and Accurate Recurrent Neural Network Acoustic Models for Speech Recognition</em>, arXiv:1507.06947 2015 [<a href="http://arxiv.org/pdf/1507.06947v1.pdf">Paper</a>].</li>
</ul>

<h3>
<a id="machine-translation" class="anchor" href="#machine-translation" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Machine Translation</h3>

<ul>
<li>Oxford [<a href="http://nal.co/papers/KalchbrennerBlunsom_EMNLP13">Paper</a>]

<ul>
<li>Nal Kalchbrenner and Phil Blunsom, <em>Recurrent Continuous Translation Models</em>, EMNLP 2013</li>
</ul>
</li>
<li>Univ. Montreal 

<ul>
<li>Kyunghyun Cho, Bart van Berrienboer, Caglar Gulcehre, Dzmitry Bahdanau, Fethi Bougares, Holger Schwenk, and Yoshua Bengio, <em>Learning Phrase Representations using RNN Encoder-Decoder for Statistical Machine Translation</em>, arXiv:1406.1078 / EMNLP 2014 [<a href="http://arxiv.org/pdf/1406.1078">Paper</a>]</li>
<li>Kyunghyun Cho, Bart van Merrienboer, Dzmitry Bahdanau, and Yoshua Bengio, <em>On the Properties of Neural Machine Translation: Encoder-Decoder Approaches</em>, SSST-8 2014 [<a href="http://www.aclweb.org/anthology/W14-4012">Paper</a>]</li>
<li>Jean Pouget-Abadie, Dzmitry Bahdanau, Bart van Merrienboer, Kyunghyun Cho, and Yoshua Bengio, <em>Overcoming the Curse of Sentence Length for Neural Machine Translation using Automatic Segmentation</em>, SSST-8 2014</li>
<li>Dzmitry Bahdanau, KyungHyun Cho, and Yoshua Bengio, <em>Neural Machine Translation by Jointly Learning to Align and Translate</em>, arXiv:1409.0473 / ICLR 2015 [<a href="http://arxiv.org/pdf/1409.0473">Paper</a>]</li>
<li>Sebastian Jean, Kyunghyun Cho, Roland Memisevic, and Yoshua Bengio, <em>On using very large target vocabulary for neural machine translation</em>, arXiv:1412.2007 / ACL 2015 [<a href="http://arxiv.org/pdf/1412.2007.pdf">Paper</a>]</li>
</ul>
</li>
<li>Univ. Montreal + Middle East Tech. Univ. + Univ. Maine [<a href="http://arxiv.org/pdf/1503.03535.pdf">Paper</a>]

<ul>
<li>Caglar Gulcehre, Orhan Firat, Kelvin Xu, Kyunghyun Cho, Loic Barrault, Huei-Chi Lin, Fethi Bougares, Holger Schwenk, and Yoshua Bengio, <em>On Using Monolingual Corpora in Neural Machine Translation</em>, arXiv:1503.03535</li>
</ul>
</li>
<li>Google [<a href="http://papers.nips.cc/paper/5346-sequence-to-sequence-learning-with-neural-networks.pdf">Paper</a>]

<ul>
<li>Ilya Sutskever, Oriol Vinyals, and Quoc V. Le, <em>Sequence to Sequence Learning with Neural Networks</em>, arXiv:1409.3215 / NIPS 2014</li>
</ul>
</li>
<li>Google + NYU [<a href="http://arxiv.org/pdf/1410.8206">Paper</a>]

<ul>
<li>Minh-Thang Luong, Ilya Sutskever, Quoc V. Le, Oriol Vinyals, and Wojciech Zaremba, <em>Addressing the Rare Word Problem in Neural Machine Transltaion</em>, arXiv:1410.8206 / ACL 2015</li>
</ul>
</li>
<li>ICT + Huawei [<a href="http://arxiv.org/pdf/1506.06442.pdf">Paper</a>]

<ul>
<li>Fandong Meng, Zhengdong Lu, Zhaopeng Tu, Hang Li, and Qun Liu, <em>A Deep Memory-based Architecture for Sequence-to-Sequence Learning</em>, arXiv:1506.06442 </li>
</ul>
</li>
<li>Stanford [<a href="http://arxiv.org/pdf/1508.04025.pdf">Paper</a>]

<ul>
<li>Minh-Thang Luong, Hieu Pham, and Christopher D. Manning, <em>Effective Approaches to Attention-based Neural Machine Translation</em>, arXiv:1508.04025</li>
</ul>
</li>
<li>Middle East Tech. Univ. + NYU + Univ. Montreal [<a href="http://arxiv.org/pdf/1601.01073.pdf">Paper</a>]

<ul>
<li>Orhan Firat, Kyunghyun Cho, and Yoshua Bengio, <em>Multi-Way, Multilingual Neural Machine Translation with a Shared Attention Mechanism</em>, arXiv:1601.01073</li>
</ul>
</li>
</ul>

<h3>
<a id="conversation-modeling" class="anchor" href="#conversation-modeling" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Conversation Modeling</h3>

<ul>
<li>Lifeng Shang, Zhengdong Lu, and Hang Li, <em>Neural Responding Machine for Short-Text Conversation</em>, arXiv:1503.02364 / ACL 2015 [<a href="http://arxiv.org/pdf/1503.02364">Paper</a>]</li>
<li>Oriol Vinyals and Quoc V. Le, <em>A Neural Conversational Model</em>, arXiv:1506.05869 [<a href="http://arxiv.org/pdf/1506.05869">Paper</a>]</li>
<li>Ryan Lowe, Nissan Pow, Iulian V. Serban, and Joelle Pineau, <em>The Ubuntu Dialogue Corpus: A Large Dataset for Research in Unstructured Multi-Turn Dialogue Systems</em>, arXiv:1506.08909 [<a href="http://arxiv.org/pdf/1506.08909">Paper</a>]</li>
</ul>

<h3>
<a id="image-captioning" class="anchor" href="#image-captioning" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Image Captioning</h3>

<ul>
<li>UCLA + Baidu [<a href="http://www.stat.ucla.edu/%7Ejunhua.mao/m-RNN.html">Web</a>] [<a href="http://arxiv.org/pdf/1410.1090">Paper-arXiv1</a>], [<a href="http://arxiv.org/pdf/1412.6632">Paper-arXiv2</a>]

<ul>
<li>Junhua Mao, Wei Xu, Yi Yang, Jiang Wang, and Alan L. Yuille, <em>Explain Images with Multimodal Recurrent Neural Networks</em>, arXiv:1410.1090</li>
<li>Junhua Mao, Wei Xu, Yi Yang, Jiang Wang, Zhiheng Huang, and Alan L. Yuille, <em>Deep Captioning with Multimodal Recurrent Neural Networks (m-RNN)</em>, arXiv:1412.6632 / ICLR 2015</li>
</ul>
</li>
<li>Univ. Toronto [<a href="http://arxiv.org/pdf/1411.2539">Paper</a>] [<a href="http://deeplearning.cs.toronto.edu/i2t">Web demo</a>]

<ul>
<li>Ryan Kiros, Ruslan Salakhutdinov, and Richard S. Zemel, <em>Unifying Visual-Semantic Embeddings with Multimodal Neural Language Models</em>, arXiv:1411.2539 / TACL 2015</li>
</ul>
</li>
<li>Berkeley [<a href="http://jeffdonahue.com/lrcn/">Web</a>] [<a href="http://arxiv.org/pdf/1411.4389">Paper</a>]

<ul>
<li>Jeff Donahue, Lisa Anne Hendricks, Sergio Guadarrama, Marcus Rohrbach, Subhashini Venugopalan, Kate Saenko, and Trevor Darrell, <em>Long-term Recurrent Convolutional Networks for Visual Recognition and Description</em>, arXiv:1411.4389 / CVPR 2015</li>
</ul>
</li>
<li>Google [<a href="http://arxiv.org/pdf/1411.4555">Paper</a>]

<ul>
<li>Oriol Vinyals, Alexander Toshev, Samy Bengio, and Dumitru Erhan, <em>Show and Tell: A Neural Image Caption Generator</em>, arXiv:1411.4555 / CVPR 2015</li>
</ul>
</li>
<li>Stanford <a href="http://cs.stanford.edu/people/karpathy/deepimagesent/">[Web]</a> <a href="http://cs.stanford.edu/people/karpathy/cvpr2015.pdf">[Paper]</a>

<ul>
<li>Andrej Karpathy and Li Fei-Fei, <em>Deep Visual-Semantic Alignments for Generating Image Description</em>, CVPR 2015</li>
</ul>
</li>
<li>Microsoft [<a href="http://arxiv.org/pdf/1411.4952">Paper</a>]

<ul>
<li>Hao Fang, Saurabh Gupta, Forrest Iandola, Rupesh Srivastava, Li Deng, Piotr Dollar, Jianfeng Gao, Xiaodong He, Margaret Mitchell, John C. Platt, Lawrence Zitnick, and Geoffrey Zweig, <em>From Captions to Visual Concepts and Back</em>, arXiv:1411.4952 / CVPR 2015</li>
</ul>
</li>
<li>CMU + Microsoft [<a href="http://arxiv.org/pdf/1411.5654">Paper-arXiv</a>], [<a href="http://www.cs.cmu.edu/%7Exinleic/papers/cvpr15_rnn.pdf">Paper-CVPR</a>]

<ul>
<li>Xinlei Chen, and C. Lawrence Zitnick, <em>Learning a Recurrent Visual Representation for Image Caption Generation</em>
</li>
<li>Xinlei Chen, and C. Lawrence Zitnick, <em>Mind’s Eye: A Recurrent Visual Representation for Image Caption Generation</em>, CVPR 2015</li>
</ul>
</li>
<li>Univ. Montreal + Univ. Toronto [<a href="http://kelvinxu.github.io/projects/capgen.html">Web</a>] [<a href="http://www.cs.toronto.edu/%7Ezemel/documents/captionAttn.pdf">Paper</a>]

<ul>
<li>Kelvin Xu, Jimmy Lei Ba, Ryan Kiros, Kyunghyun Cho, Aaron Courville, Ruslan Salakhutdinov, Richard S. Zemel, and Yoshua Bengio, <em>Show, Attend, and Tell: Neural Image Caption Generation with Visual Attention</em>, arXiv:1502.03044 / ICML 2015</li>
</ul>
</li>
<li>Idiap + EPFL + Facebook [<a href="http://arxiv.org/pdf/1502.03671">Paper</a>]

<ul>
<li>Remi Lebret, Pedro O. Pinheiro, and Ronan Collobert, <em>Phrase-based Image Captioning</em>, arXiv:1502.03671 / ICML 2015</li>
</ul>
</li>
<li>UCLA + Baidu [<a href="http://arxiv.org/pdf/1504.06692">Paper</a>]

<ul>
<li>Junhua Mao, Wei Xu, Yi Yang, Jiang Wang, Zhiheng Huang, and Alan L. Yuille, <em>Learning like a Child: Fast Novel Visual Concept Learning from Sentence Descriptions of Images</em>, arXiv:1504.06692</li>
</ul>
</li>
<li>MS + Berkeley

<ul>
<li>Jacob Devlin, Saurabh Gupta, Ross Girshick, Margaret Mitchell, and C. Lawrence Zitnick, <em>Exploring Nearest Neighbor Approaches for Image Captioning</em>, arXiv:1505.04467 (Note: technically not RNN) [<a href="http://arxiv.org/pdf/1505.04467.pdf">Paper</a>]</li>
<li>Jacob Devlin, Hao Cheng, Hao Fang, Saurabh Gupta, Li Deng, Xiaodong He, Geoffrey Zweig, and Margaret Mitchell, <em>Language Models for Image Captioning: The Quirks and What Works</em>, arXiv:1505.01809 [<a href="http://arxiv.org/pdf/1505.01809.pdf">Paper</a>]</li>
</ul>
</li>
<li>Adelaide [<a href="http://arxiv.org/pdf/1506.01144.pdf">Paper</a>]

<ul>
<li>Qi Wu, Chunhua Shen, Anton van den Hengel, Lingqiao Liu, and Anthony Dick, <em>Image Captioning with an Intermediate Attributes Layer</em>, arXiv:1506.01144</li>
</ul>
</li>
<li>Tilburg [<a href="http://arxiv.org/pdf/1506.03694.pdf">Paper</a>]

<ul>
<li>Grzegorz Chrupala, Akos Kadar, and Afra Alishahi, <em>Learning language through pictures</em>, arXiv:1506.03694</li>
</ul>
</li>
<li>Univ. Montreal [<a href="http://arxiv.org/pdf/1507.01053.pdf">Paper</a>]

<ul>
<li>Kyunghyun Cho, Aaron Courville, and Yoshua Bengio, <em>Describing Multimedia Content using Attention-based Encoder-Decoder Networks</em>, arXiv:1507.01053</li>
</ul>
</li>
<li>Cornell [<a href="http://arxiv.org/pdf/1508.02091.pdf">Paper</a>]

<ul>
<li>Jack Hessel, Nicolas Savva, and Michael J. Wilber, <em>Image Representations and New Domains in Neural Image Captioning</em>, arXiv:1508.02091</li>
</ul>
</li>
</ul>

<h3>
<a id="video-captioning" class="anchor" href="#video-captioning" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Video Captioning</h3>

<ul>
<li>Berkeley [<a href="http://jeffdonahue.com/lrcn/">Web</a>] [<a href="http://arxiv.org/pdf/1411.4389">Paper</a>]

<ul>
<li>Jeff Donahue, Lisa Anne Hendricks, Sergio Guadarrama, Marcus Rohrbach, Subhashini Venugopalan, Kate Saenko, and Trevor Darrell, <em>Long-term Recurrent Convolutional Networks for Visual Recognition and Description</em>, arXiv:1411.4389 / CVPR 2015</li>
</ul>
</li>
<li>UT Austin + UML + Berkeley [<a href="http://arxiv.org/pdf/1412.4729">Paper</a>]

<ul>
<li>Subhashini Venugopalan, Huijuan Xu, Jeff Donahue, Marcus Rohrbach, Raymond Mooney, and Kate Saenko, <em>Translating Videos to Natural Language Using Deep Recurrent Neural Networks</em>, arXiv:1412.4729</li>
</ul>
</li>
<li>Microsoft [<a href="http://arxiv.org/pdf/1505.01861">Paper</a>]

<ul>
<li>Yingwei Pan, Tao Mei, Ting Yao, Houqiang Li, and Yong Rui, <em>Joint Modeling Embedding and Translation to Bridge Video and Language</em>, arXiv:1505.01861</li>
</ul>
</li>
<li>UT Austin + Berkeley + UML [<a href="http://arxiv.org/pdf/1505.00487">Paper</a>]

<ul>
<li>Subhashini Venugopalan, Marcus Rohrbach, Jeff Donahue, Raymond Mooney, Trevor Darrell, and Kate Saenko, <em>Sequence to Sequence--Video to Text</em>, arXiv:1505.00487</li>
</ul>
</li>
<li>Univ. Montreal + Univ. Sherbrooke [<a href="http://arxiv.org/pdf/1502.08029.pdf">Paper</a>]

<ul>
<li>Li Yao, Atousa Torabi, Kyunghyun Cho, Nicolas Ballas, Christopher Pal, Hugo Larochelle, and Aaron Courville, <em>Describing Videos by Exploiting Temporal Structure</em>, arXiv:1502.08029</li>
</ul>
</li>
<li>MPI + Berkeley [<a href="http://arxiv.org/pdf/1506.01698.pdf">Paper</a>]

<ul>
<li>Anna Rohrbach, Marcus Rohrbach, and Bernt Schiele, <em>The Long-Short Story of Movie Description</em>, arXiv:1506.01698</li>
</ul>
</li>
<li>Univ. Toronto + MIT [<a href="http://arxiv.org/pdf/1506.06724.pdf">Paper</a>]

<ul>
<li>Yukun Zhu, Ryan Kiros, Richard Zemel, Ruslan Salakhutdinov, Raquel Urtasun, Antonio Torralba, and Sanja Fidler, <em>Aligning Books and Movies: Towards Story-like Visual Explanations by Watching Movies and Reading Books</em>, arXiv:1506.06724</li>
</ul>
</li>
<li>Univ. Montreal [<a href="http://arxiv.org/pdf/1507.01053.pdf">Paper</a>]

<ul>
<li>Kyunghyun Cho, Aaron Courville, and Yoshua Bengio, <em>Describing Multimedia Content using Attention-based Encoder-Decoder Networks</em>, arXiv:1507.01053</li>
</ul>
</li>
<li>Zhejiang Univ. + UTS [<a href="http://arxiv.org/abs/1511.03476">Paper</a>]

<ul>
<li>Pingbo Pan, Zhongwen Xu, Yi Yang, Fei Wu, Yueting Zhuang, <em>Hierarchical Recurrent Neural Encoder for Video Representation with Application to Captioning</em>, arXiv:1511.03476</li>
</ul>
</li>
<li>Univ. Montreal + NYU + IBM [<a href="http://arxiv.org/pdf/1511.04590.pdf">Paper</a>]

<ul>
<li>Li Yao, Nicolas Ballas, Kyunghyun Cho, John R. Smith, and Yoshua Bengio, <em>Empirical performance upper bounds for image and video captioning</em>, arXiv:1511.04590</li>
</ul>
</li>
</ul>

<h3>
<a id="video-modeling" class="anchor" href="#video-modeling" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Video Modeling</h3>

<ul>
<li>Univ. Toronto [<a href="http://arxiv.org/abs/1502.04681">paper</a>]

<ul>
<li>Nitish Srivastava, Elman Mansimov, Ruslan Salakhutdinov, Unsupervised Learning of Video Representations using LSTMs, arXiv:1502.04681 / ICML 2015</li>
</ul>
</li>
<li>Univ. Cambridge [<a href="http://arxiv.org/abs/1511.06309">paper</a>]

<ul>
<li>Viorica Patraucean, Ankur Handa, Roberto Cipolla, Spatio-temporal video autoencoder with differentiable memory, arXiv:1511.06309</li>
</ul>
</li>
</ul>

<h3>
<a id="question-answering" class="anchor" href="#question-answering" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Question Answering</h3>

<ul>
<li>FAIR [<a href="https://research.facebook.com/researchers/1543934539189348">Web</a>] [<a href="http://arxiv.org/pdf/1502.05698.pdf">Paper</a>]

<ul>
<li>Jason Weston, Antoine Bordes, Sumit Chopra, Tomas Mikolov, and Alexander M. Rush, <em>Towards AI-Complete Question Answering: A Set of Prerequisite Toy Tasks</em>, arXiv:1502.05698</li>
</ul>
</li>
<li>Virginia Tech. + MSR [<a href="http://www.visualqa.org/">Web</a>] [<a href="http://arxiv.org/pdf/1505.00468">Paper</a>]

<ul>
<li>Stanislaw Antol, Aishwarya Agrawal, Jiasen Lu, Margaret Mitchell, Dhruv Batra, C. Lawrence Zitnick, and Devi Parikh, <em>VQA: Visual Question Answering</em>, arXiv:1505.00468 / CVPR 2015 SUNw:Scene Understanding workshop</li>
</ul>
</li>
<li>MPI + Berkeley [<a href="https://www.mpi-inf.mpg.de/departments/computer-vision-and-multimodal-computing/research/vision-and-language/visual-turing-challenge/">Web</a>] [<a href="http://arxiv.org/pdf/1505.01121">Paper</a>]

<ul>
<li>Mateusz Malinowski, Marcus Rohrbach, and Mario Fritz, <em>Ask Your Neurons: A Neural-based Approach to Answering Questions about Images</em>, arXiv:1505.01121</li>
</ul>
</li>
<li>Univ. Toronto [<a href="http://arxiv.org/pdf/1505.02074">Paper</a>] [<a href="http://www.cs.toronto.edu/%7Emren/imageqa/data/cocoqa/">Dataset</a>]

<ul>
<li>Mengye Ren, Ryan Kiros, and Richard Zemel, <em>Exploring Models and Data for Image Question Answering</em>, arXiv:1505.02074 / ICML 2015 deep learning workshop</li>
</ul>
</li>
<li>Baidu + UCLA [<a href="http://arxiv.org/pdf/1505.05612">Paper</a>] [<a href="">Dataset</a>]

<ul>
<li>Hauyuan Gao, Junhua Mao, Jie Zhou, Zhiheng Huang, Lei Wang, and Wei Xu, <em>Are You Talking to a Machine? Dataset and Methods for Multilingual Image Question Answering</em>, arXiv:1505.05612 / NIPS 2015</li>
</ul>
</li>
<li>DeepMind + Oxford [<a href="http://arxiv.org/pdf/1506.03340.pdf">Paper</a>]

<ul>
<li>Karl M. Hermann, Tomas Kocisky, Edward Grefenstette, Lasse Espeholt, Will Kay, Mustafa Suleyman, and Phil Blunsom, <em>Teaching Machines to Read and Comprehend</em>, arXiv:1506.03340 / NIPS 2015</li>
</ul>
</li>
<li>MetaMind [<a href="http://arxiv.org/pdf/1506.07285.pdf">Paper</a>]

<ul>
<li>Ankit Kumar, Ozan Irsoy, Jonathan Su, James Bradbury, Robert English, Brian Pierce, Peter Ondruska, Mohit Iyyer, Ishaan Gulrajani, and Richard Socher, <em>Ask Me Anything: Dynamic Memory Networks for Natural Language Processing</em>, arXiv:1506.07285</li>
</ul>
</li>
<li>Video QA

<ul>
<li>CMU + UTS [<a href="http://arxiv.org/abs/1511.04670">paper</a>]

<ul>
<li>Linchao Zhu, Zhongwen Xu, Yi Yang, Alexander G. Hauptmann, Uncovering Temporal Context for Video Question and Answering, arXiv:1511.04670</li>
</ul>
</li>
<li>KIT + MIT + Univ. Toronto [<a href="http://arxiv.org/abs/1512.02902">Paper</a>] [<a href="http://movieqa.cs.toronto.edu/home/">Dataset</a>]

<ul>
<li>Makarand Tapaswi, Yukun Zhu, Rainer Stiefelhagen, Antonio Torralba, Raquel Urtasun, Sanja Fidler, MovieQA: Understanding Stories in Movies through Question-Answering, arXiv:1512.02902</li>
</ul>
</li>
</ul>
</li>
</ul>

<h3>
<a id="image-generation" class="anchor" href="#image-generation" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Image Generation</h3>

<ul>
<li>Karol Gregor, Ivo Danihelka, Alex Graves, Danilo J. Rezende, and Daan Wierstra, <em>DRAW: A Recurrent Neural Network for Image Generation,</em> ICML 2015 [<a href="http://arxiv.org/pdf/1502.04623">Paper</a>]</li>
<li>Angeliki Lazaridou, Dat T. Nguyen, R. Bernardi, and M. Baroni, <em>Unveiling the Dreams of Word Embeddings: Towards Language-Driven Image Generation,</em> arXiv:1506.03500 [<a href="http://arxiv.org/pdf/1506.03500">Paper</a>]</li>
<li>Lucas Theis and Matthias Bethge, <em>Generative Image Modeling Using Spatial LSTMs,</em> arXiv:1506.03478 / NIPS 2015 [<a href="http://arxiv.org/pdf/1506.03478">Paper</a>]</li>
<li>Aaron van den Oord, Nal Kalchbrenner, and Koray Kavukcuoglu, <em>Pixel Recurrent Neural Networks,</em> arXiv:1601.06759 [<a href="http://arxiv.org/abs/1601.06759">Paper</a>]</li>
</ul>

<h3>
<a id="turing-machines" class="anchor" href="#turing-machines" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Turing Machines</h3>

<ul>
<li> A.Graves, G. Wayne, and I. Danihelka., <em>Neural Turing Machines,</em> arXiv preprint arXiv:1410.5401 [<a href="http://arxiv.org/pdf/1410.5401">Paper</a>]</li>
<li>Jason Weston, Sumit Chopra, Antoine Bordes, <em>Memory Networks,</em> arXiv:1410.3916 [<a href="http://arxiv.org/pdf/1410.3916">Paper</a>]</li>
<li>Armand Joulin and Tomas Mikolov, <em>Inferring Algorithmic Patterns with Stack-Augmented Recurrent Nets</em>, arXiv:1503.01007 / NIPS 2015 [<a href="http://arxiv.org/pdf/1503.01007">Paper</a>]</li>
<li>Sainbayar Sukhbaatar, Arthur Szlam, Jason Weston, and Rob Fergus, <em>End-To-End Memory Networks</em>, arXiv:1503.08895 / NIPS 2015 [<a href="http://arxiv.org/pdf/1503.08895">Paper</a>]</li>
<li>Wojciech Zaremba and Ilya Sutskever, <em>Reinforcement Learning Neural Turing Machines,</em> arXiv:1505.00521 [<a href="http://arxiv.org/pdf/1505.00521">Paper</a>]</li>
<li>Baolin Peng and Kaisheng Yao, <em>Recurrent Neural Networks with External Memory for Language Understanding</em>, arXiv:1506.00195 [<a href="http://arxiv.org/pdf/1506.00195.pdf">Paper</a>]</li>
<li>Fandong Meng, Zhengdong Lu, Zhaopeng Tu, Hang Li, and Qun Liu, <em>A Deep Memory-based Architecture for Sequence-to-Sequence Learning</em>, arXiv:1506.06442 [<a href="http://arxiv.org/pdf/1506.06442.pdf">Paper</a>]</li>
<li>Arvind Neelakantan, Quoc V. Le, and Ilya Sutskever, <em>Neural Programmer: Inducing Latent Programs with Gradient Descent</em>, arXiv:1511.04834 [<a href="http://arxiv.org/pdf/1511.04834.pdf">Paper</a>]</li>
<li>Scott Reed and Nando de Freitas, <em>Neural Programmer-Interpreters</em>, arXiv:1511.06279 [<a href="http://arxiv.org/pdf/1511.06279.pdf">Paper</a>]</li>
<li>Karol Kurach, Marcin Andrychowicz, and Ilya Sutskever, <em>Neural Random-Access Machines</em>, arXiv:1511.06392 [<a href="http://arxiv.org/pdf/1511.06392.pdf">Paper</a>]</li>
<li>Łukasz Kaiser and Ilya Sutskever, <em>Neural GPUs Learn Algorithms</em>, arXiv:1511.08228 [<a href="http://arxiv.org/pdf/1511.08228.pdf">Paper</a>]</li>
<li>Ethan Caballero, <em>Skip-Thought Memory Networks</em>, arXiv:1511.6420 [<a href="arxiv.org/pdf/1511.06420.pdf">Paper</a>]</li>
<li>Wojciech Zaremba, Tomas Mikolov, Armand Joulin, and Rob Fergus, <em>Learning Simple Algorithms from Examples</em>, arXiv:1511.07275 [<a href="http://arxiv.org/pdf/1511.07275.pdf">Paper</a>]</li>
</ul>

<h3>
<a id="robotics" class="anchor" href="#robotics" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Robotics</h3>

<ul>
<li>Hongyuan Mei, Mohit Bansal, and Matthew R. Walter, <em>Listen, Attend, and Walk: Neural Mapping of Navigational Instructions to Action Sequences</em>, arXiv:1506.04089 [<a href="http://arxiv.org/pdf/1506.04089.pdf">Paper</a>]</li>
<li>Marvin Zhang, Sergey Levine, Zoe McCarthy, Chelsea Finn, and Pieter Abbeel, <em>Policy Learning with Continuous Memory States for Partially Observed Robotic Control,</em> arXiv:1507.01273. <a href="http://arxiv.org/pdf/1507.01273">[Paper]</a>
</li>
</ul>

<h3>
<a id="other" class="anchor" href="#other" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Other</h3>

<ul>
<li>Alex Graves, <em>Generating Sequences With Recurrent Neural Networks,</em> arXiv:1308.0850 <a href="http://arxiv.org/abs/1308.0850">[Paper]</a>
</li>
<li>Volodymyr Mnih, Nicolas Heess, Alex Graves, and Koray Kavukcuoglu, <em>Recurrent Models of Visual Attention</em>, NIPS 2014 / arXiv:1406.6247 [<a href="http://arxiv.org/pdf/1406.6247.pdf">Paper</a>]</li>
<li>Wojciech Zaremba and Ilya Sutskever, <em>Learning to Execute</em>, arXiv:1410.4615 [<a href="http://arxiv.org/pdf/1410.4615.pdf">Paper</a>] [<a href="https://github.com/wojciechz/learning_to_execute">Code</a>]</li>
<li>Samy Bengio, Oriol Vinyals, Navdeep Jaitly, and Noam Shazeer, <em>Scheduled Sampling for Sequence Prediction with
Recurrent Neural Networks</em>, arXiv:1506.03099 / NIPS 2015 [<a href="http://arxiv.org/pdf/1506.03099">Paper</a>]</li>
<li>Bing Shuai, Zhen Zuo, Gang Wang, and Bing Wang, <em>DAG-Recurrent Neural Networks For Scene Labeling</em>, arXiv:1509.00552 [<a href="http://arxiv.org/pdf/1509.00552">Paper</a>]</li>
<li>Soren Kaae Sonderby, Casper Kaae Sonderby, Lars Maaloe, and Ole Winther, <em>Recurrent Spatial Transformer Networks</em>, arXiv:1509.05329 [<a href="http://arxiv.org/pdf/1509.05329">Paper</a>]</li>
<li>Cesar Laurent, Gabriel Pereyra, Philemon Brakel, Ying Zhang, and Yoshua Bengio, <em>Batch Normalized Recurrent Neural Networks</em>, arXiv:1510.01378 [<a href="http://arxiv.org/pdf/1510.01378">Paper</a>]</li>
<li>Jiwon Kim, Jung Kwon Lee, Kyoung Mu Lee, <em>Deeply-Recursive Convolutional Network for Image Super-Resolution</em>, arXiv:1511.04491 <a href="http://arxiv.org/abs/1511.04491">[Paper]</a>
</li>
<li>Quan Gan, Qipeng Guo, Zheng Zhang, and Kyunghyun Cho, <em>First Step toward Model-Free, Anonymous Object Tracking with Recurrent Neural Networks</em>, arXiv:1511.06425 [<a href="http://arxiv.org/pdf/1511.06425.pdf">Paper</a>]</li>
<li>Francesco Visin, Kyle Kastner, Aaron Courville, Yoshua Bengio, Matteo Matteucci, and Kyunghyun Cho, <em>ReSeg: A Recurrent Neural Network for Object Segmentation</em>, arXiv:1511.07053 [<a href="http://arxiv.org/pdf/1511.07053.pdf">Paper</a>]</li>
<li>Juergen Schmidhuber, <em>On Learning to Think: Algorithmic Information Theory for Novel Combinations of Reinforcement Learning Controllers and Recurrent Neural World Models</em>, arXiv:1511.09249 <a href="http://arxiv.org/pdf/1511.09249">[Paper]</a>
</li>
</ul>

<h2>
<a id="datasets" class="anchor" href="#datasets" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Datasets</h2>

<ul>
<li>Speech Recognition

<ul>
<li>
<a href="http://www.openslr.org/resources.php">OpenSLR</a> (Open Speech and Language Resources)

<ul>
<li><a href="http://www.openslr.org/12/">LibriSpeech ASR corpus</a></li>
</ul>
</li>
<li><a href="http://voxforge.org/home">VoxForge</a></li>
</ul>
</li>
<li>Image Captioning

<ul>
<li><a href="http://nlp.cs.illinois.edu/HockenmaierGroup/Framing_Image_Description/KCCA.html">Flickr 8k</a></li>
<li><a href="http://shannon.cs.illinois.edu/DenotationGraph/">Flickr 30k</a></li>
<li><a href="http://mscoco.org/home/">Microsoft COCO</a></li>
</ul>
</li>
<li>Image Question Answering

<ul>
<li>
<a href="https://www.mpi-inf.mpg.de/departments/computer-vision-and-multimodal-computing/research/vision-and-language/visual-turing-challenge/">DAQUAR</a> - built upon <a href="http://cs.nyu.edu/%7Esilberman/datasets/nyu_depth_v2.html">NYU Depth v2</a> by N. Silberman et al.</li>
<li>
<a href="http://www.visualqa.org/">VQA</a> - based on <a href="http://mscoco.org/">MSCOCO</a> images</li>
<li>
<a href="http://www.cs.toronto.edu/%7Emren/imageqa/data/cocoqa/">Image QA</a> - based on MSCOCO images</li>
<li>[Multilingual Image QA] - built from scratch by Baidu - in Chinese, with English translation</li>
</ul>
</li>
<li>Action Recognition

<ul>
<li>
<a href="http://www.thumos.info/home.html">THUMOS</a> : Large-scale action recognition dataset</li>
<li>
<a href="http://ai.stanford.edu/%7Esyyeung/resources/multithumos.zip">MultiTHUMOS</a> : Extension of THUMOS '14 action detection dataset with dense multilabele annotation</li>
</ul>
</li>
</ul>

<h2>
<a id="blogs" class="anchor" href="#blogs" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Blogs</h2>

<ul>
<li>
<a href="http://karpathy.github.io/2015/05/21/rnn-effectiveness/">The Unreasonable Effectiveness of RNNs</a> by <a href="http://cs.stanford.edu/people/karpathy/">Andrej Karpathy</a>
</li>
<li>
<a href="http://colah.github.io/posts/2015-08-Understanding-LSTMs/">Understanding LSTM Networks</a> in <a href="http://colah.github.io/">Colah's blog</a>
</li>
<li>
<a href="http://www.wildml.com/">WildML</a> blog's RNN tutorial [<a href="http://www.wildml.com/2015/09/recurrent-neural-networks-tutorial-part-1-introduction-to-rnns/">Part1</a>], [<a href="http://www.wildml.com/2015/09/recurrent-neural-networks-tutorial-part-2-implementing-a-language-model-rnn-with-python-numpy-and-theano/">Part2</a>], [<a href="http://www.wildml.com/2015/10/recurrent-neural-networks-tutorial-part-3-backpropagation-through-time-and-vanishing-gradients/">Part3</a>], [<a href="http://www.wildml.com/2015/10/recurrent-neural-network-tutorial-part-4-implementing-a-grulstm-rnn-with-python-and-theano/">Part4</a>]</li>
<li>
<a href="https://svail.github.io/">Optimizing RNN Performance</a> from Baidu's Silicon Valley AI Lab.</li>
<li>
<a href="http://nbviewer.ipython.org/gist/yoavg/d76121dfde2618422139">Character Level Language modelling using RNN</a> by Yoav Goldberg</li>
<li>
<a href="http://peterroelants.github.io/posts/rnn_implementation_part01/">Implement an RNN in Python</a>. </li>
<li><a href="http://arunmallya.github.io/writeups/nn/lstm/index.html#/">LSTM Backpropogation</a></li>
</ul>

<h2>
<a id="online-demos" class="anchor" href="#online-demos" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Online Demos</h2>

<ul>
<li>Alex graves, hand-writing generation [<a href="http://www.cs.toronto.edu/%7Egraves/handwriting.html">link</a>]</li>
<li>Ink Poster: Handwritten post-it notes [<a href="http://www.inkposter.com/?">link</a>]</li>
</ul>
