# ４８の感情うちどの感情が含まれているのかを分析できるコードです。
言語商会・長岡技術科学大学、山本先生の日本語感情表現辞書( https://www.jnlp.org/GengoHouse/snow/d18 )を用いて感情分析を行います。
山本先生のコーパスは単語に対して被験者の３人が48の感情のうちどの感情を感じたかが記されています。このコーパスを用いることで、文章に含まれている最も強い感情を特定することが可能です。
例えば、夏目漱石さんの「こころ」（青空文庫（　https://www.aozora.gr.jp/　）を分析すると解析結果は次のような感じになります。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2847349/148cce5c-431b-0c30-4581-ad4bfe50d081.png)

# プログラムの構成
文章の形態素解析には自然言語処理ライブラリGiNZAを用いました。GiNZAはリクルートさんと国立国語研究所さんが開発したものであり、高精度な解析が可能なライブラリです。
形態素解析で単語に分割した後、言語商会・長岡技術科学大学山本先生の日本語感情表現辞書( https://www.jnlp.org/GengoHouse/snow/d18 )に検索をかけます。そして、単語ごとに含まれている感情を抽出し、文全体の感情を計測します。

# This code could analyze which emotions are included among 48 emotions.
By using the japanese emotions dictionary ( https://www.jnlp.org/GengoHouse/snow/d18 ), you could analyze emotions.
This program is using GiNZA which could do high-precision analysis.
