# 名前空間は省略する

SVGやMathMLはHTMLの文書では直接扱えます。

悪い例:

    <svg xmlns="http://www.w3.org/2000/svg">
      ...
    </svg>

良い例:

    <svg>
      ...
    </svg>


## 解説

HTML5でもXHTML 1.1のように名前空間を指定して拡張できます。XML構文を使う必要がありますが、今まで通り`xmlns`属性を使うだけです。

    <div>
      <svg xmlns="http://www.w3.org/2000/svg" version="1.1">
        ...
      </svg>
    </div>

SVGやMathMLに関しては限定的ではありますがインラインで利用できるように仕様で定義されており、指定する必要はまったくありません。

    <div>
      <svg version="1.1">
        ...
      </svg>
    </div>

もちろん必要ならばHTML文書をXML構文で書くように修正しつつ、名前空間を利用して拡張するべきではあります。しかしXHTML 2.0の策定が頓挫した理由の1つとして、柔軟な拡張がそれほど求められていなかったことが挙げられるように、名前空間を指定してまで拡張する機会はまずないはずです。