# The Calkin Algebra as a Test for Nuclearity

Hikaru Awazu（粟津 光）

連絡先: huhihikaru@gmail.com

- [最新版 PDF](docs/The_Calkin_Algebra_as_a_Test_for_Nuclearity_public.pdf)（LaTeX ソースを内蔵）
- [LaTeX ソース](docs/The_Calkin_Algebra_as_a_Test_for_Nuclearity_public.tex)
- [検証状況](VERIFICATION_STATUS.md)
- [GitHub Pages](https://unti-fourier.github.io/calkin-proof-candidate/)

固定した Calkin 代数 \(Q=\mathcal B(\ell^2)/\mathcal K(\ell^2)\) に対し、標準写像 \(B\otimes_{\max}Q\to B\otimes_{\min}Q\) が単射であることと、複素 \(C^*\) 代数 \(B\) が核的であることの同値を示します。\(B\) の単位性、可分性、事前の exactness は仮定しません。

今回の改訂では、従来のランプ群の構成を自由群の語長による減衰に置き換え、finite な von Neumann 環上の一つのテンソルに対する相関と最小ノルムの差を直接示します。途中で、exact な \(B\) では右因子 \(C_r^*(\mathbb F_2)\) でも核性を判定できることを示します。

この証明は GPT-6 を用いて作成し、改訂した書面証明は別々の AI による検算を経ています。改訂版の主定理は Lean で検証済みです。査読は未実施です。形式化の範囲は[検証状況](VERIFICATION_STATUS.md)を参照してください。

## Previous version

The [V80 plaintext manuscript](manuscript/calkin-test-candidate.txt), [previous GitHub snapshot](https://github.com/unti-fourier/calkin-proof-candidate/tree/73741ad9f671034fd94a8dc827e691b05b9bab69), and [previous Zenodo release](https://doi.org/10.5281/zenodo.24362321) remain available. The current PDF and TeX on GitHub use the revised argument.
