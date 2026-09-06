# Six Optimization Algorithms, Built from Scratch

<details>
<summary>🇹🇷 Türkçe özet için tıklayın</summary>

Üç bağımsız optimizasyon problemi, hepsinde `scipy.optimize` gibi hazır kütüphane fonksiyonları yerine algoritmalar **sıfırdan** yazılmış ve karşılaştırmalı olarak analiz edilmiş.

**Soru 1, elips uydurma:** 200 veri noktasına 5 parametreli bir elips modeli uydurma problemi. Jacobian matrisi elle türetildi, Gauss-Newton ve Levenberg-Marquardt algoritmaları sıfırdan yazılıp yakınsama hızı ve koşul sayısı üzerinden karşılaştırıldı.

**Soru 2, global optimizasyon:** çok sayıda yerel minimuma sahip bir hedef fonksiyonun global minimumunu bulma problemi. Particle Swarm Optimization ve Genetik Algoritma sıfırdan yazıldı, 25 bağımsız denemeyle istatistiksel karşılaştırma yapıldı, gürültülü versiyonda sağlamlık test edildi, farklı değerlendirme bütçeleri altında performans karşılaştırıldı.

**Soru 3, gradyan tabanlı optimizasyon:** Fletcher-Reeves (Conjugate Gradient) ve Newton's Method sıfırdan yazıldı, backtracking line search ile. Üç farklı başlangıç noktasından yakınsama davranışı ve Hessian koşul sayısının optimizasyon yolu boyunca değişimi incelendi.

</details>

Three independent optimization problems. In every one, the algorithm itself is written from scratch instead of calling a library function like `scipy.optimize`, since the point was to understand the algorithm, not just get an answer.

## Problem 1: ellipse fitting (nonlinear least squares)

Fitting a five-parameter ellipse model (center, semi-axes, rotation angle) to 200 data points in `data.txt`. The Jacobian is derived by hand. Gauss-Newton and Levenberg-Marquardt are both implemented from scratch and compared on convergence speed and condition number.

## Problem 2: the dolphin function (global optimization)

Finding the global minimum of an objective function with many local minima, parameterized by student ID. Particle Swarm Optimization and a Genetic Algorithm are both built from scratch. The comparison includes 25 independent runs for statistical comparison (success rate, mean and standard deviation), a robustness test on a noisy version of the function, performance across different evaluation budgets (750, 1000, 1500), and success rate at finding the global minimum from random sub-regions.

## Problem 3: the Beale function (gradient-based optimization)

Fletcher-Reeves (a conjugate gradient method) and Newton's Method, both built from scratch with backtracking line search. Compares convergence behavior from three different starting points (close to the minimum, far from it, and one where the Hessian is singular), and tracks how the Hessian's condition number changes along the optimization path.

## Files

| File | What it is |
|---|---|
| `hw2.ipynb` | The main notebook: all code, plots, and written analysis |
| `data.txt` | The 200 ellipse data points used in Problem 1 |
| `hw2.pdf` | A PDF export of the notebook |
| `Optimization_2025_2026_HW2.pdf` | The original problem statement |

## Tools

Python, NumPy, Matplotlib. `scipy.optimize` and similar ready-made optimizers were deliberately not used, the goal was implementing the algorithms themselves.
