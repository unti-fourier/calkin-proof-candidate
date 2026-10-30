# Calkin test conjecture — 未査読の証明案

**これは未査読・未認定の証明案です。本人が今後、人力で検証する予定ですが、検証には時間を要します。自動検査で具体的な穴が特定されなかったことは、証明の認定を意味しません。**

**Hikaru Awazu（粟津 光）**  
Assistant Professor, National Institute of Technology, Hakodate College  
連絡先: [huhihikaru@gmail.com](mailto:huhihikaru@gmail.com)

Lean による形式化も別途進行中です。完全な形式検証が完了したという主張はしていません。

この資料は、Calkin test conjecture に関心を持った人が、概要と証明案の全文を読めるようにするためのものです。対象は作用素代数、C*-algebras、nuclearity（核性）、exactness、local lifting property（LLP）に関係する問題です。検索エンジンや AI への収録・発見可能性を保証するものではありません。

- [証明案の全文（V80、プレーンテキスト）](manuscript/calkin-test-candidate.txt)
- [検証状況と数学補足の位置づけ](VERIFICATION_STATUS.md)

## 問題と提案する主張

可分無限次元 Hilbert 空間 $`H=\ell^2(\mathbb N)`$ を固定し、その Calkin 代数を

$$
Q=\mathcal B(H)/\mathcal K(H)
$$

とします。任意の複素 $`C^*`$ 代数 $`B`$ に対し、代数的テンソル積上の恒等写像から定まる標準的な全射 $`*`$ 準同型

$$
\chi_B:B\otimes_{\max}Q\longrightarrow B\otimes_{\min}Q
$$

を考えます。本稿が証明を提案している主張は

$$
\chi_B\text{ が単射}\quad\Longleftrightarrow\quad B\text{ が核的}
$$

です。$`B`$ の単位性・可分性・sigma-unitality・事前の exactness は仮定しません。単射性は**完備化されたテンソル積の間**での主張であり、指定された代数的テンソル積上の max/min ノルム一致と同値です。

核性から単射性への向きは定義から従います。本稿の新規の証明案は逆向きを対象とし、仮説から元の $`B`$ の exactness を得た後、非核性を仮定して矛盾を導く構成です。

## 証明案の構成

| 部分 | 提案する役割 | 対象を保つための要点 |
| --- | --- | --- |
| **G：一般入力** | 小さい空間テンソルノルムを持つ有限ユニタリ族と、大きな左右相関を持つ一つの正常状態を供給する。 | 最終データは同一の角 $`N=eB^{**}e`$ に置く。type III の増幅は、その角と状態を固定する前に吸収する。 |
| **E：cocycle の評価** | 元の cyclic-lamp 構成から、全有限語・全標的ベクトルに共通する $`L^2`$ 評価を得る。 | 共有ランプ、逆辺、非可換積順序を保持する。別々の語全体が独立であるとは仮定しない。 |
| **M：モーメント写像** | 指定モーメントとブロックの trace ideal の消滅を、一つの UCP 写像で同時に実現する。 | reduced 商への因子化、正常な源側延長、有限モデルの忠実なコピー、trace-GNS 回復を区別する。 |
| **D：元の代数への移送** | 元の $`B`$ 内の係数を選び、一つの固定状態を保つ exactness 切断から正の核元を作る。 | Goldstine 近似は標準的な二重双対 $`B^{**}`$ の正常汎関数を使う。結論の代数を増幅や単位化に置き換えない。 |

ここで E は検査時の係数評価の呼称です。本文中で標準 exactness 定理に付けられたラベル `(E)` とは区別します。UCP は unital completely positive（単位的完全正）を意味します。

論証が正しければ、同じ自己共役元 $`u`$ と固定状態 $`\Psi`$ に対して

$$
\|u\|_{\max}\leq1,\qquad \|u\|_{\min}<7/8,\qquad
\Psi(u)>251/256
$$

が得られ、最大テンソル積内の連続関数計算によって

$$
k=(u-7/8)_+,\qquad \chi_B(k)=0,\qquad
\Psi(k)>27/256,\qquad \|k\|_{\max}\leq1/8
$$

という非零の正の核元が生じる、という構成です。$`k`$ 自身が有限な代数的テンソルであるとは主張しません。この帰結は、提案した補題と接続の正しさに依存します。

## 標準定理と新規の論証

標準入力として、Kirchberg の exactness 判定、Choi–Effros の核性と標準的な二重双対の単射性の同値、Haagerup の有限 von Neumann 代数判定、標準形・自然錐の平方根不等式、modular core の半有限性、Takesaki 双対性を採用しています。GNS/Stinespring、Kaplansky、Hahn–Banach、Goldstine、関数計算等も用います。文献と適用する形は全文の第1節・参考文献に記載しています。

**G/M/D と E/HS の新規論証を、既知の標準定理として採用しているわけではありません。** 自動読解では、調べた依存関係に具体的な反例や未供給の必須仮定は特定されませんでした。しかし共通の推論誤り、量化順序、無限次元での適用条件の見落としは排除できません。検査回数や保存ファイルのハッシュは数学的正しさの根拠にはなりません。

独立した人間による査読や、完成した Lean 証明は主張していません。本人による人力検証と進行中の形式化も、現時点の証明認定とは区別します。最新文献の網羅的調査、優先権、投稿予定についても主張していません。

## Short English overview

**Unreviewed proof candidate. Hikaru Awazu plans to verify the argument manually; this will take time. Automated checks finding no specific gap do not certify a proof. Lean formalization is in progress; no complete formal verification is claimed.**

This work proposes a proof of the fixed Calkin tensor test: for an arbitrary complex C*-algebra $`B`$, the canonical map $`B\otimes_{\max}Q\to B\otimes_{\min}Q`$, with $`Q=\mathcal B(\ell^2)/\mathcal K(\ell^2)`$, is injective if and only if $`B`$ is nuclear. No unitality, separability, or initial exactness of $`B`$ is assumed. The candidate combines a bidual-corner input, a cyclic-lamp cocycle estimate, one completely positive moment map, and an exactness cut preserving a fixed state. Related topics include nuclearity, exactness, and the local lifting property (LLP). The full argument is available through the manuscript link above. Neither mathematical correctness nor search-engine or AI indexing is guaranteed.
