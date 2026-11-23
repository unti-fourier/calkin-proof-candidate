# 検証状況 / Verification status

## 改訂版：自由群の語長を用いる証明

[PDF](docs/The_Calkin_Algebra_as_a_Test_for_Nuclearity_public.pdf)・[LaTeX](docs/The_Calkin_Algebra_as_a_Test_for_Nuclearity_public.tex)

- 書面証明：固定した Calkin 代数から exactness と LLP を得る部分、左側が正常なテンソル積テストへの移送、finite な von Neumann 環への帰着、自由群の語長による減衰と最小ノルム計算を記載しています。改訂した論証を別々の AI による書面検算で確認しました。
- 査読・人による検証：査読は受けていません。AI による検算は人による独立した査読ではありません。
- 改訂版の Lean：形式化を開始しましたが、改訂版全体の形式検証は完了していません。

## 旧版：V80

[V80 プレーンテキスト](manuscript/calkin-test-candidate.txt)・[旧版の検証記録](https://github.com/unti-fourier/calkin-proof-candidate/blob/73741ad9f671034fd94a8dc827e691b05b9bab69/VERIFICATION_STATUS.md)

旧版ではランプ群を用いた別の証明を検討しました。旧版の主定理と採用した依存関係を Lean でソースから再ビルドした記録は、旧ルートに固有です。その記録によって、改訂した書面証明が Lean で検証済みになるわけではありません。
