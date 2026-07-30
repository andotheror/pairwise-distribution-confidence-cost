# The Confidence Cost of Pairwise Distribution Learning

## Abstract

Pairwise conditional access to an unknown distribution returns a draw from the distribution restricted to any requested pair. At constant confidence, this weak oracle is as sample-efficient for labeled total-variation learning as ordinary sampling, up to constants. We show that this equivalence fails at high confidence.

For a distribution on $n$ labels, accuracy $\varepsilon$, and failure probability $\delta$, we prove the exact minimax query complexity

$$
\Theta\left(\frac{n\log(1/\delta)}{\varepsilon^2}\right).
$$

The corresponding ordinary-sampling complexity is $\Theta((n+\log(1/\delta))/\varepsilon^2)$. Thus confidence amplification costs up to a factor $n$ under pairwise access.

The upper bound reuses one trajectory of a pairwise-winner Markov chain whose stationary law is the target. Although its worst-case relaxation time is linear in $n$, we prove that its empirical distribution has the i.i.d.-scale stationary risk $O(\sqrt{n/T})$. The proof compares its conductances with a minimum-mass graph. After sorting the target probabilities, this graph has an explicit Helmert eigensystem, and a capped-mass Green-function bound telescopes without any minimum-mass or dynamic-range assumption. A geometric median of independent trajectories gives the high-confidence result. The lower bound uses a heavy label and uniform light labels. Every adaptive pair query then carries only $O(\varepsilon^2/n)$ KL information, which makes the multiplicative confidence cost unavoidable.

## Main results

**Theorem (Minimax pairwise learning).** There are universal constants $c,C>0$ such that, for $n\ge 4$, $0<\varepsilon\le 1/16$, and $0<\delta\le 1/8$,

$$
c\frac{n\log(1/\delta)}{\varepsilon^2} \le q_{\mathrm{pair}}(n,\varepsilon,\delta) \le C\frac{n\log(1/\delta)}{\varepsilon^2}.
$$

The upper bound is attained by a polynomial-time adaptive learner and allows arbitrary zero probabilities.

**Theorem (Stationary occupation risk).** Let $(X_t)_{t=1}^T$ be a stationary trajectory of the pairwise-winner chain, and let $\widehat p_T$ be its empirical law. For every $p\in\Delta_n$,

$$
\mathbb{E}_p\,\mathrm{TV}(\widehat p_T,p) \le (2+2\sqrt{2})\sqrt{\frac{n}{T}}.
$$

## Files

- `main.pdf` — the paper.
- `supplement.pdf` — full proofs and the deterministic verification audit.
- `*.ots` — OpenTimestamps proofs establishing the existence date of each file.
