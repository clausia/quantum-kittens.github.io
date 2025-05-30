---
title: '第2章 - 解説 - 量子ビット, 重ね合わせ, 測定'
math: true
---



古典コンピューティングとは、ほとんどの人が「コンピューティング」と言ったときに指すもののことです。例えば、いまあなたがこの文章を読むのに使っているような日常的な電子機器によって行われる計算であり、研究室にあるスーパーコンピュータによって行われる計算も含みます。

古典的なコンピューターの場合、情報の基本単位は「ビット」によって運ばれます。これは、2つの値または「状態」のうちの1つだけを持つことができる情報の最小単位で0か1かの2値しか持ちません。 これと同じように、量子コンピューターにも、「量子ビット」と呼ばれる基本的な情報の単位があります。ウィスカートンのビー玉も、実は量子ビットと同じものを表しているのです。

## 量子ビットとは?

量子ビットは、量子コンピューターにおいて最も単純な系であり、量子コンピューターの基本的な構成要素です。量子ビットは物理的には、量子コンピューターが使用するハードウェアによって、さまざまな方式で実現できます。しかし、どのような方式でも、動作的には同じように動作します。つまり、「量子ビット」とは、古典的なビットとは異なる不思議な振る舞いをする抽象的な数学的オブジェクトであると考えることができます。古典的なビットは、0と1の2つの値のどちらかを取ることができますが、量子ビットはそれ以上のことをすることができるのです。

> 量子ビットは、0と1の状態だけでなく、その2つの状態の「重ね合わせ」を取ることができる抽象的な数学的なオブジェクトです。
{: .prompt-tip }

##  量子重ね合わせ

量子重ね合わせは、古典物理学にはみられない、量子物理学の現象です。重ね合わせは一種の「組み合わせ」だと考えることができます。

古典的なビットは0か1のどちらかの状態でなければならず、2つの状態を組み合わせることはできませんが、量子ビットは組み合わせても有効な状態にすることができます。つまり、量子ビットの状態は、0と1の組み合わせが可能なのです。

![](/assets/imgs/Marble_Animation.png){: style="max-width: 150px" .left} ウィスカートンでは、ビー玉は赤と青が同じ重み付けで組み合わせた状態になっています。ただ、この色を絵の具の色と同じだと考えるのは間違いです。例えば、赤と青の絵の具を組み合わせると、紫色の絵の具になります。そして混ぜた結果の紫色の絵の具からはもはや赤や青の色は単色取り出せませんよね？しかし、ウィスカートンのビー玉を住民猫が直接観察すると、50パーセントの確率で赤色に、50パーセントの確率で青色に変化し、けっして紫色にはなりません。必ず赤か青、どちらか一方の色になります。

この不思議な現象を利用できることが、量子コンピューターと古典コンピューターの違いの1つです。古典的なコンピューターでは、ビットに対して演算を行う場合、基本的に0か1のどちらか一方に対して演算を行うことになります。もしも、その両方に対して演算を行う必要がある場合は、2回に分けて連続して演算を行う必要があります。

しかし、量子コンピューターは、重ね合わせの原理を利用することで、0と1の両方に対して同時に演算を行うことができるのです。これを多くの量子ビットに拡張すれば、計算の高速化、メモリ容量の増加などの改良につながる可能性があることはご想像いただけると思います。

## 測定

ビー玉を直接観察すると、50％の確率で赤や青になることがわかりましたね。猫がビー玉を観察するのは、赤が1、青が0を表す量子ビットの状態を測定することのたとえです。実際の測定は、実験室で物理量を測定することで行われます。

測定は、基本的に量子ビットがどのような状態にあるかを確認することですが、注意点があります。測定という行為は、量子ビットを0か1のどちらかの状態に落ち着かせることになるので、0か1かの答えしか得られないのです。しかし、その結果には必ず確率が付随します。

たとえ確率のすべてを事前に知っていたとしても、つまり、測定前に量子ビットの正確な重ね合わせ状態を知っていたとしても、測定結果を予測することはできないのです。

基本的には:

> たとえある量子系の状態をすべて知っていたとしても、量子系はランダムに振る舞う可能性があります。
{: .prompt-tip }

例えば、ウィスカートンのビー玉の状態がすべてわかっているとしましょう。それは、等しい重さ（確率）が50パーセントずつの重ね合わせの状態です。しかし、測定後、それが赤いビー玉となるか、青いビー玉のどちらになるかはわかりません。そこがランダムな部分です。

量子物理学は確率論的であり、それは「不確実性」があることを意味します。測定という行為によってはじめて、物理系は不確実から確実へと移行します。

一見すると、古典的なビットと同じように、最終的な結果は0と1しか得られないので、量子重ね合わせの利点がなくなってしまったように見えるかもしれません。そこで登場したのが、量子コンピューティングのアルゴリズムです。

アルゴリズムとは、基本的に、ある結果を得るために行う一連の操作のことです。量子コンピューティングのアルゴリズムは、確率を操作して、目的の結果に関連する確率を上げ、それ以外の確率を下げるものです。[^footnote] この方法では、目的の状態に関連する確率が1になると、その結果が保証されることになり、その動作はもはやランダムではないことを意味します。

[^footnote]: 量子演算は「量子ゲート」と呼ばれるものを用いて行います。量子ゲートとは、量子回路の構成要素であり、従来のデジタル回路における古典的な論理ゲートに相当する論理演算を行うものです。

ここまでで、量子ビット、量子重ね合わせ、測定の概要をお伝えしました。これでウィスカートンのビー玉の背後にある物理が分かったと思います。 

>ブレイドの置かれた苦境が、いわゆる「シュレーディンガーの猫」とどのように関係しているのか、これらの概念をより深く掘り下げたい方はこのまま読み進めてください。そうでなければ、次の物語へどうぞ: [第3章 - 物語 - ドアベル](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)
{: .prompt-info }

_______


## 量子ビットの状態の数学的表現

量子状態は、数学的には「ディラック記法」と呼ばれる方法で表現され、ケット: $\ket{}$[^fn-nth-1] と呼ばれる記号を活用します。: $\ket{}$[^fn-nth-1].

[^fn-nth-1]: ケットは、*ベクトル*と呼ばれる特定の性質を持つ数学的な物体を表します。量子ビットはベクトルと見なすことができます。2つのベクトルを組み合わせて、別の有効なベクトルを形成することができます。しかし、この文章を読むのにベクトルについて知る必要はありません。

任意の量子ビットの状態は、次のように表現されます。[^fn-nth-2]:

\begin{equation}
\label{eq:qubit}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

[^fn-nth-2]: 免責事項：上記式は量子ビットの全体像ではありません。量子ビットにはさらに「位相」という自由度があり、これも計算に有用ですが、この文章の範囲外になっています。

ギリシア文字 $\psi$ は「サイ」と発音し, 量子状態を象徴的に表現したものです。$\ket{}$ 記号は表記として登場しますが、読みとしては特に発声しません。  量子ビットに言及する場合、式で $ket{psi}$ を定義した後、「量子ビットがサイという量子状態にあります」と発声したり「量子状態 $ket{psi}$ 」と記述したりすることが可能です。

ケット記号の中に収まっているのは $\psi$ だけではないことに注意してください。0と1の状態である $\ket{0}$ と $\ket{1}$ も方程式に含まれていますね。これらは、量子ビットの *固有状態*と呼ばれ、ウィスカートンのビー玉が赤や青に帰着するように、測定後に量子ビットが帰着する可能性のある状態を指します。 1つの量子ビットが2つの固有状態を持つので、量子ビットは2準位系と呼ばれます。

プラス記号は組み合わせ、つまり重ね合わせを表します。パラメータ $\alpha_{0}$ と $\alpha_{1}$ は*確率振幅*と呼ばれ、測定後に量子ビットが $\ket{0}$ または $\ket{1}$ の状態になる確率を表します（ $\alpha$ はギリシャ文字のアルファです）。この記号 $\alpha$ の添え字は、どの基底状態に対応するかを示すラベルです。

数学的には、確率振幅を2乗すれば、各基底状態に関連する確率が得られます。つまり、量子ビットを $\ket{\psi}$ の状態で測定すると、確率 $\alpha_{0}^2$ で0、確率 $\alpha_{1}^2$ で1の結果が得られることになります。[^fn-nth-3］ 

[^fn-nth-3]: 上付き添え字の2は「二乗」を表し、数字が自分自身に掛けられることを意味します。つまり、$\alpha_{0}^2=\alpha_{0}*\alpha_{0}$ のことを言います。

なぜ突然このような四角いものが出てくるのか不思議に思うかもしれません。これは、振幅 $\alpha_{0}$ と $\alpha_{1}$ が負である可能性があることを思い出させる数学的な慣習に過ぎないのです。それぞれの振幅の2乗は確率で、確率は常に正であり、2乗も正なのです。

これは、各量子状態が制約を受けることを意味します。確率論では、すべての確率は足し算で 1 になるという厳格なルールがあるので、*常に $\alpha_{0}^2+\alpha_{1}^2=1$ となります。

具体的な例を見てみましょう。量子ビットが下記のようなある状態だとします。

\begin{equation}
\ket{\psi}=\sqrt{\frac{2}{3}}\ket{0}-\sqrt{\frac{1}{3}}\ket{1}
\end{equation}

ここで、 $\alpha_{0}=\sqrt{\frac{2}{3}}$ であり、測定後に結果0を得る確率は $\frac{2}{3}$ です。同様に、$\alpha_{1}=-\sqrt{\frac{1}{3}}$ となり、結果1に関連する確率は $\frac{1}{3}$ となります。つまり、この状態の量子ビットが大量にあり、それらをすべて測定した場合、統計的にはおよそ3分の1が結果 1 をもたらすことになります。振幅が大きい$\alpha$ ほど確率が高くなり、測定後に関連する状態の量子ビットが見つかる可能性が高くなります。[^fn-nth-4]

[^fn-nth-4]: 数学者のためのメモ：ここでは $mod(\alpha)$ と表記します。

## 統計に関する注意点

量子ビットの特徴は、任意の状態 $\ket{\psi}$$ の $\alpha_{0}$ と $\alpha_{1}$ を測定で決定できないことで、これらの $\alpha$ の数を正確に知るには、その状態を自分で作ったか、作った人を知っている必要があります。なぜなら、測定の結果は常に1つだからです。0 か 1 であるから、どのような測定も $\alpha$ の知識にはつながりません。もし誰かがその状態を作ったのであれば、同じ状態の量子ビットを何千個も用意してもらい、何千回も測定した後、その状態の振幅、つまり確率が何であるかを統計的に解読することができます。[^fn-nth-5］

[^fn-nth-5]: 量子回路を何度も実行するのは、まさにそのためであり、統計を取るためです。量子回路とは、量子計算のモデルであり、ゲート配列や測定などの演算子が存在します。

しかし、量子ビットが有用であるためには、必ずしも $\alpha$ が何であるかを知っている必要はありません。量子ビットの美しさは、測定前に量子ゲートで$alpha_{0}$と$alpha_{1}$を変化させて操作できることにあります。前述のとおり、ゴールは得たい結果に関連する確率を高めることです。もし、望む結果が 0 であれば、それが何であれ、$\alpha_{0}$ を増幅するようにアルゴリズムを設計することができます。また、 $\alpha_{0} = 1$ であれば、結果 0 が保証されることになります。

## 物理的な量子ビット

先に述べたように、量子状態は数学的な要素で構成されているため、量子ビットそのものを形づくる物理系に依存することなく、アルゴリズム開発などのために数学的に扱うことが容易になっているのです。これは重要なことで、量子状態を、例えば電子のスピンや光子の偏光状態など、どのような方式で物理的に構築したとしても、同じ数学表現でその状態を表すことができるのです。

電子や光子とは何なのでしょうか？わからない人のために、簡単に解説しておきましょう。

> 電子とは、負の電荷を帯びた素粒子です。電子には「スピン」と呼ばれる性質がありますが、ここでは詳しく理解する必要はありません。電子のスピンは $+\frac{1}{2}$ または $-\frac{1}{2}$ であり、数学的には $\ket{0}$ と $\ket{1}$ という状態で表される、ということだけ理解すれば十分でしょう。
{: .prompt-info }


>光子は、可視光線を含む電磁波の構成要素です。あなたが見ているものはすべて、この光子が網膜に当たることで像を結びます。この光子が「偏光」されると、全方向ではなく、特定の方向に振動するようになります。量子ビットで言うと、例えば横方向の偏光は $\ket{0}$ 、縦方向の偏光は $\ket{1}$ で表すことができます。そしてそれぞれの偏光状態は、重ね合わせが可能であり、光子が垂直方向と水平方向の中間で振動していることに相当します（コンパスの南と東の間にある南東のようなものです）。
{: .prompt-info }


量子ビットの状態について注意すべき重要な点は、量子ビットは安定ではないということです。量子ビットは、環境におけるちょっとした乱れ、例えば熱や振動などの乱れによって、 $\ket{0}$ または $\ket{1}$ のどちらかになってしまうのです[^fn-nth-6]。量子ビットを研究室で操作するのが少し厄介なのは、このような状態の綱引きがあるからで、ウィスカートンの猫たちが興味をそそられるのは、そうした量子状態の性質にです！

[^fn-nth-6]: このような量子状態のもつ繊細さは、安定的に動作する物理量子ビットや、多数の量子ビットを保有するデバイスを構築する上で克服すべき課題の一つです。しかし、この分野は、多くの有望な進展が見られるエキサイティングな研究分野です。

## シュレーディンガーの猫

ここで、キラキラマシンと共に箱の中にいる猫のブレイドの話に戻りましょう。彼の苦境は、1935年に物理学者エルヴィン・シュレーディンガーが行った思考実験へのオマージュのようなものです。[^fn-nth-7].

[^fn-nth-7]: Schrödinger, Erwin (November 1935). "Die gegenwärtige Situation in der Quantenmechanik (The present situation in quantum mechanics)". Naturwissenschaften. 23 (48): 807-812.

量子ビットは２準位系であり、2つの基底状態を持つが、それ以上の基底状態を持つ量子や量子システムも存在します。しかし、量子ビットを含むこれらの系はすべて、測定時に、すべての可能性の中から1つだけ結果を出すという点では、同じ原理に基づいています。

なぜ、このようなことが起こるのか、本当のところは誰も知りません。1つ考えられるのは、量子力学のコペンハーゲン解釈と呼ばれる考えです。この解釈では、測定という行為自体が、あらゆる可能性を1つに縮減してしまいます。1935年、物理学者エルヴィン・シュレーディンガーは、この解釈への反証として、ミクロの世界の量子効果をマクロの世界である猫に外挿するという有名な思考実験を論文で発表しました。

本来の思考実験では、量子ビット（あるいはウィスカートンのビー玉）の代わりに放射性物質が使われます。放射性物質は、量子ビットが確率に従ってある状態に還元されるのと同じように、確率に従って崩壊します。

毒薬の入った瓶と連動した放射性物質を入れた箱の中に猫を入れます。もし放射性原子の1つでも崩壊すれば、毒薬瓶は粉々になり、結果として猫は毒殺されてしまいます。このように、猫の状態は、少なくとも1つの原子が崩壊する確率に支配される毒物系の状態と連動しているのです。このとき、箱を開けるまでの間は、猫は死んでいるとも生きているとも考えられます。つまり、箱が開けられる前は、猫の状態は未確定です。

シュレーディンガーは、これは「ばかげた話」として、箱を開ける前に猫が死んでいるのと生きているのとが重ね合わされた状態にあるなどとは、とても信じられないことだと主張したのでした。もちろん、彼の言う通りです。この思考実験の前提は、真に量子的とは言えません。なぜなら猫は量子と同一ではないのですから。この思考実験は、猫が生死をさまよっている話なのではなく、あくまでも確率的なシステムについて説明しようとするものです。

いずれにせよ、この思考実験は、大衆文化における量子現象の最も認知された図像のひとつとなり、当然ウィスカートンにも登場することになりました。もちろん、このような趣のある小さな町に毒々しい話はにつかわしくありませんから、ここはきらびやかに。なお、シュレーディンガーは単に思考実験としてこうした喩えを思いついただけで、猫に実際に毒を盛ったりすることはありませんでしたので、ご安心ください。

さて、この思考実験にはもう一つ不思議な点があります。それは、猫の状態が放射性物質の状態と*もつれ*状態にあると言えることです。

量子もつれは、われわれの次の目的地です! さっそく行ってみましょう。「第3章 - 物語 - 呼び鈴」へ。: **[ 第3章 - 物語 - 呼び鈴](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)**

_____________________________


_____________________________


_____________________________




## Qiskit Code

This section is for those of you who want to get started with Qiskit, IBM Quantum’s open source python framework to program quantum computers.

You can simulate a Whiskerton marble using this supplementary Qiskit code. This code walks you through creating and running a quantum circuit with a single qubit.

You can run this code in two ways:

- On the cloud: you can choose use a cloud-based tool like [Google Colab](https://colab.research.google.com/) or [qBraid](https://www.qbraid.com/). 
- Locally: you can [install Qiskit](https://qiskit.org/) and run the code on your local machine

See this blog post for further setup details: [
Explore newly recommended notebook environments for Qiskit](https://www.ibm.com/quantum/blog/qiskit-notebook-environments)

The below code is also available as a jupyter notebook [here](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_2.ipynb).

November 2024 note: this code has now been updated to Qiskit 1.0. If you've used an earlier version of Qiskit before, this blog post may be useful for you: [Best practices for transitioning to Qiskit SDK v1.0](https://www.ibm.com/quantum/blog/transition-to-1)





 ```python
# Install Qiskit along with some optional dependencies useful for visualization 
# by uncommenting the instruction below if you don't have Qiskit installed already

#pip install'qiskit[visualization]'

# Install the Qiskit Runtime Service if you don't have it installed already by uncommenting the instruction below

#pip install qiskit-ibm-runtime

# Install the Qiskit Aer Simulator if you don't have it installed already by uncommenting the instruction below

#pip install qiskit-aer

# Import necessary Qiskit libraries

from qiskit import QuantumCircuit

#Create Marble Circuit

marble_circuit = QuantumCircuit(1, 1) # add one qubit (Whiskerton marble) and one classical bit (to store the measurement outcome)

marble_circuit.h(0) # add H-gate or Hadamard gate to the qubit (this is the quantum gate that puts the marble in superposition)

marble_circuit.measure(0,0) # add a measurement operator (this is equivalent to a cat looking directly at a marble)

marble_circuit.draw('mpl') # see how the circuit looks
```



 ```python

 # Import necessary Qiskit libraries for running the circuit on a simulator

from qiskit.transpiler.preset_passmanagers import generate_preset_pass_manager
from qiskit_ibm_runtime import QiskitRuntimeService
from qiskit_aer import AerSimulator
from qiskit_ibm_runtime import SamplerV2 as Sampler
from qiskit.visualization import plot_histogram


#Run Marble Circuit,
#That is, see if the marble turns red or blue

marble_state = {'1': 'red', '0': 'blue'}

aer_sim = AerSimulator() # Identify the quantum computer to run this on. In this case it's a simulator not a real device.
pm = generate_preset_pass_manager(backend=aer_sim, optimization_level=1) 
isa_marble_circuit = pm.run(marble_circuit) # This line and the line above essentially prepare the circuit to be executed on the device you selected. For for more technical details, please see: https://docs.quantum.ibm.com/api/qiskit/transpiler#transpiler

# fetch and print the outcome:
sampler = Sampler(mode=aer_sim)

result = sampler.run([isa_marble_circuit], shots=1000).result() # Run the circuit on the simulator 1000 times to gather statistics.
counts = result[0].data.c.get_counts()

ans = str(max(counts, key=counts.get))

print('The marble is ' + marble_state[ans] + '.') # The outcome is the one associated with the highest count.



```

```python

# Examine the statistics and plot histogram

print("Your result in the form of counts:", counts)
print("Thus, in 1000 shots, you get blue " + str(counts['0']) + " times, and red " + str(counts['1']) + " times.")

plot_histogram(counts)

```

```python
# If you want to run the circuit on a real device then you can use the following 

#from qiskit_ibm_runtime import QiskitRuntimeService
 
#service = QiskitRuntimeService(channel="ibm_quantum", token="<insert your token here>")
```



*Note: the Qiskit code provided is open source, and does not fall under the copyright of Quantum Kittens.*