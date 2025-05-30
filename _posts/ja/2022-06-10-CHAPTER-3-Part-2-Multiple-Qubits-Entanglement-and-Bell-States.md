---
title: '第３章 - 解説 - 複数量子ビット, もつれ, ベル状態について'
math: true
---


古典的なビット一つができることはあまりありません。情報処理やアルゴリズムには、通常、より多くの情報単位が必要です。例えば、あなたがソーシャルメディアにアップする画像は1ビットで表現できません。多くの0と1の長いビット列で表現され、そのビット列がインターネットを通じて送信され、あなたのデバイスで処理されるのです。 

それと同じように、量子ビットがどんなに革新的なものに見えても、1つの量子ビットでできることはそれほど多くはありません。実際、量子コンピューターが古典的なコンピューターより優位に立てるのは、安定したエラーのない量子ビットを何百、何千と持つプロセッサを作れるようになってからです。

したがって、量子コンピューターのプロトコルは、ウィスカートンの玄関の呼び鈴がビー玉を2個以上使っているように、2個以上の量子ビットを使うものがほとんどである。確かに、ウィスカートンのドアベルはビー玉が2つしかない非常に単純な量子システムだが、将来の量子コンピュータのアルゴリズムには、それ以上のビー玉が必要なものもある。しかし、このドアベルは、より複雑なプロトコルが利用する、古典的世界では類似点のない量子現象「量子もつれ」を示している。 

## 量子もつれとは何か？ 

量子もつれは、量子系間の特異な相関関係をあらわします。2つの量子系がもつれた場合、それらの状態は独立して記述することができないような形で存在し、一方の量子で測定を行うと、たとえもう一方の量子が近くになくても、瞬時に影響し状態が確定します。

つまり、量子の世界では次のようなことが可能になります：

> 2つの量子ビット（または量子系）が互いに影響を及ぼせないほど遠く離れていても、一方を観察するともう一方に直ちに影響を及ぼすような相関関係を持つことがあります。 
{: .prompt-tip }


ウィスカートンの呼び鈴を構成する2つのビー玉はもつれ状態にあります。１つ目が赤くなると、２つ目のビー玉も別の箱に入っていても同じように赤くなることを覚えておいてください。２つ目のビー玉が一色に定まるためには、２つ目のビー玉を直接見る必要はありません。

この「量子もつれ」は、私たちが日常生活で目にする相関関係とは全く異なるものです。古典的な世界では、不透明な袋に赤と青の2つのビー玉が入っていて、青い方を取り出すと、赤い方がまだ袋の中にあることがすぐにわかるはずです。これが古典的な相関関係であり、私たちが日常的に体験している相関関係です。


しかし、量子もつれは、古典的な相関関係とは異なる振る舞いをします。私たちが日常的に経験しない特徴があるのです。たとえば、ビー玉がウイスカートンのビー玉であれば、そもそも一色にはなりません。袋から取り出したビー玉は、見るまでは重ね合わせの状態になっているはずです。手の中のビー玉が単一色に還元されて初めて、袋の中のビー玉は、たとえ遠くへ持っていかれても変化するのです。[^fn-nth-1] 

[^fn-nth-1]: もつれには他にも特徴があり、非常に離れた2つの量子系が互いに影響し合うには、いわゆる非局所的でなければなりませんが、それはまた別の日に探求することにしましょう。 

また、あなたはここで不思議に思っているかもしれません。二つの系が距離にかかわらず瞬時に影響しあうということは、つまり、光よりも速く情報を送れるということなのだろうか？残念ながら、答えは「いいえ」です。 

量子の状態を観測する際、通常の測定を行うだけではうまくいきません。そう、測定と一口にいっても様々な種類があります！測定の種類については本文の範囲外になりますが、もしあなたと遠くに住む友人がもつれた量子ペアを共有しているならば、あなたが自分のペアで行う測定の種類について、何らかの方法で友人に伝えなければならない、とだけ理解しておけばここでは十分です。もし、あなたの友人が、どのような測定を行うべきかを知らなければ、期待される結果を「見る」ことはできません。だから、何らかの方法で、例えば電話で伝える必要があります。ただし、光より速いスピードの伝達はできません。

>量子もつれについてもう少し深く知りたい方は、こちらをお読みください。それ以外の方は、次のページに進んでください。: [This is Not the End](https://quantum-kittens.github.io/posts/This-is-not-the-end/).
{: .prompt-info }


_______

## 複数量子ビット状態の数学的表現

複数量子ビットの状態は、単一量子ビットの状態と同様の方法で表現されます。ウイスカートンの呼び鈴は2つの量子ビットを持つので、2量子ビットの状態に焦点を当てますが、ここで習う表現はより多くの量子ビットにも拡張できます。 

[第2章 - 解説 - 量子ビット, 重ね合わせ, 測定](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/)の任意の1量子ビットの状態に関する方程式を思い出してください。 :


\begin{equation}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

この式において、基底状態は古典的なビットが持ちうる2つの値と同義です。そして、量子ビットはこの2つの基底状態の重ね合わせの状態になることができます。 

2量子ビットの状態を表現する方法を理解するために、古典的な2ビットの取りうるすべての値を見てみましょう。2つのビットを組み合わせると、4つの値 00、01、10、11 のうちの1つを持つことができます。1量子ビットの場合と同じように、この4つの値は4つの基底状態に対応します。2つの量子ビットは、これら4つの状態のうちの1つになることもあれば、これらの状態の重ね合わせになることもあります。したがって、任意の2量子ビットの状態は、次の式で表すことができます。 

\begin{equation}
\ket{\psi}=\alpha_{00}\ket{00}+\alpha_{01}\ket{01}+\alpha_{10}\ket{10}+\alpha_{11}\ket{11}
\end{equation}

単一量子ビットの式と同じように、 $\alpha_{00}^2$ は2つの量子ビットが測定後に 00 という結果をもたらす確率です。他の3つの基底状態も同様です。確率の法則にもとづいて、２つの量子ビットの量子状態は以下のように記述できます。
$\alpha_{00}^2+\alpha_{01}^2+\alpha_{10}^2+\alpha_{11}^2=1$


## 量子もつれとベル状態

単に2つの量子ビットが手元にあるだけでは、それらがもつれ状態にあると見なすことはできません。量子ビットがもつれるには、特定の状態にあることが必要で、つまり、もつれを意味する特定の $\alpha$ 値が存在することになります。

例えば、ウイスカートンの呼び鈴のもつれ状態は、 $\alpha_{01}=\alpha_{10}=0$ と表現することができ、 $\alpha_{00}$ と $\alpha_{11}$ は、それらの二乗を足すと１になる必要があります。


細かくみていきましょう。ウイスカートン式呼び鈴は、外のビー玉を直接観察すると、内側のビー玉も同じ色になりました。もし、ビー玉が同じ色にしかならないのであれば、2つの状態しかありえないことになる。 $\ket{red, red}$ と $\ket{blue, blue}$ です。各 $\ket{}$ の1つ目の位置は外側のビー玉を表し、2つ目の位置は内側のビー玉を表します。状態 $\ket{red, blue}$ は違法であり、呼び鈴装置内では絶対に起こりえないので、これに伴う確率は 0  となります。 $\ket{blue, red}$ の場合も同様です。

つまり、0でない確率は $\ket{red, red}$ と $\ket{blue, blue}$ だけであり、ウイスカートンのビー玉がどちらの色になるかは半々の確率なので、この2つの確率は等しくなければなりません。 


これを記述すると以下のようになります:



\begin{equation}
\ket{\phi^+}=\frac{1}{\sqrt{2}}\ket{00}+\frac{1}{\sqrt{2}}\ket{11}
\label{eq:bellstate}
\end{equation}

このビー玉の状態は「ベル状態」と呼ばれるものです。ウイスカートンの「ドアベル」の特徴とは関係なく、物理学者ジョン・S・ベル氏にちなんで名付けられました。上の式は、この特定のベル状態が数学的にどのように見えるかを示したもので、 $\phi^+$ は命名規則になります。 [^fn-nth-2]

[^fn-nth-2]: これは、ベル状態が数学的に*計算基底*でどのように見えるかであり、結果を「見る」ために必要な測定の種類を示すものです。異なる種類の測定には、それぞれ対する異なる基底が存在します。

このように、最初の量子ビットを測定する前に、2つの基底状態 $\ket{00},\ket{11}$ のどちらかが発生する確率は等しくなっているのです。しかし、1番目の量子ビットが $\ket{0}$ or $\ket{1}$ のどちらかになると、2番目の量子ビットはそれに従わざるをえなくなります。このようにして、結果が相関し、量子ビットがもつれ状態にあります。

ここで重要なのは、これが唯一のベル状態ではなく、他のベル状態も損じするということです。例えば、他のベル状態の1つは、2番目の量子ビットが常に1番目の量子ビットと*逆の*状態になるパターンだったりします。たまたま、ウィスカートンの呼び鈴のもつれたビー玉は同じ状態になるパターンであるに過ぎません。

このようなベル状態の2量子ビットのペアは、物理学者アルバート・アインシュタイン、ボリス・ポドルスキー、ネイサン・ローゼンの名前をとって「EPRペア」と呼ばれています。EPRペアと量子もつれは、量子暗号、超密度符号、量子テレポーテーションなどの理論的および潜在的な量子コンピューティング応用のための貴重な資源です。[^fn-nth-3］ 

[^fn-nth-3]: ここで登場するテレポーテーションとは、「スタートレック」に登場するような瞬間移動のそれとは違います。テレポーテーションの応用は、今後の物語で探求してく予定です。
 
## 物理的にもつれ状態にある量子ビットに関する備考
 
実験室で量子ビットを物理的にもつれ状態にする方法は、量子ビットをどういう方法で実装するかによって決まります。例えば、1つの光源から特定の方法で生成された2つの光子が、もつれた状態で出現することがあります。ウィスカートンにあるような単一の普遍的な「エンタングラー」は存在しません。また現実には、これらの光源を「エンタングラー」と呼ぶ人はまずいないでしょう。まあ、ネコは別として。 
 
_____________________________


_____________________________


_____________________________


**[Next: This is Not the End](https://quantum-kittens.github.io/posts/This-is-not-the-end/)**
 
________

## Qiskit Code

You can simulate a Whiskerton doorbell using the following code. By using this code, you will learn how to create the quantum circuit corresponding to the Bell state.

The below code is also available as a jupyter notebook [here](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_3.ipynb).

 ```python
# Import necessary Qiskit libraries

from qiskit import QuantumCircuit, QuantumRegister, ClassicalRegister

#Create Doorbell Entangler Circuit

qubits = QuantumRegister(2, name='q') # Create a quantum register with 2 qubits (Whiskertese marbles) and name the register 'q'

classical_bits = ClassicalRegister(2, name='c') # Create a classical register with 2 bits and name the register 'c' (to eventually store the measurement outcome)

q0, q1 = qubits # Label the two qubits in the register 'q0' and 'q1'

c0, c1 = classical_bits

doorbell_circuit = QuantumCircuit(qubits, classical_bits) # Create a circuit with the quantum and classical registers.

doorbell_circuit.h(q0) # Add a Hadamard gate to the first qubit 

doorbell_circuit.cx(q0,q1) # Add a cnot gate with the first qubit as the control and the second qubit as the target. The target flips its state when the control is in the 1 state.

doorbell_circuit.measure([q0,q1],[c0,c1]) # Add measurement operators (this is equivalent to a cat looking directly at the outer marble).

doorbell_circuit.draw('mpl') # See how the circuit looks.

```


As an exercise, run this circuit in a similar way to the marble circuit in [Chapter 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/)!

*Note: the Qiskit code provided is open source, and does not fall under the copyright of Quantum Kittens.*


