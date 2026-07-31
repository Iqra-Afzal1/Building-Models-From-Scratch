# Loss Function

A suitable cost function can be chosen, I have picked Mean Squared Error.

$$\downarrow$$

$$J(\theta_0, \theta_1) = \frac{1}{2m} \sum_{i=1}^{m} \left(h_{\theta}(x^i) - y^i\right)^2$$

In future calculation, we would get '2' in numerator, so to make terms clean we append '2' in denomintor (which won't affect results).

# Algorithm

## 1. Start with some $\theta_0$ and $\theta_1$

---

## 2.
### Rule to Update $\theta_0$
$$\text{temp}_0 = \theta_0 - (LR) \times \text{slope}$$

$$= \theta_0 - (\alpha) \times \frac{d}{d\theta_0} J(\theta_0, \theta_1)$$

$$= \theta_0 - (\alpha) \times \frac{d}{d\theta_0} \left( \frac{1}{2m} \sum_{i=1}^{m} \left( h_\theta(x^i) - y^i \right)^2 \right)$$

$$= \theta_0 - (\alpha) \times \frac{d}{d\theta_0} \left( \frac{1}{2m} \sum_{i=1}^{m} \left( \theta_0 + \theta_1 x^i - y^i \right)^2 \right)$$

### Rule to Update $\theta_1$
$$\text{temp}_1 = \theta_1 - (LR) \times \text{Slope}$$

$$= \theta_1 - (\alpha) \times \frac{d}{d\theta_1} J(\theta_0, \theta_1)$$

$$= \theta_1 - (\alpha) \times \frac{d}{d\theta_1} \left( \frac{1}{2m} \sum_{i=1}^{m} \left( \theta_0 + \theta_1 x^i - y^i \right)^2 \right)$$

$$\theta_0 = \text{temp}_0$$
$$\theta_1 = \text{temp}_1$$

---

# Calculation of $\text{Slope}_{\theta_0}$ & $\text{Slope}_{\theta_1}$

### $\text{Slope}_{\theta_0}$

$$\frac{d}{d\theta_0} J(\theta_0, \theta_1) = \frac{d}{d\theta_0} \left( \frac{1}{2m} \sum_{i=1}^{m} \left( \theta_0 + \theta_1 x^i - y^i \right)^2 \right)$$

$$= \frac{1}{\cancel{2}m} \times \cancel{2} \sum_{i=1}^{m} (\theta_0 + \theta_1 x^i - y^i)(1)$$

$$\frac{d}{d\theta_0} J(\theta_0, \theta_1) = \frac{1}{m} \sum_{i=1}^{m} (\theta_0 + \theta_1 x^i - y^i)$$

*(Note: $\underbrace{\theta_0 + \theta_1 x^i}_{h(x_i)}$)*

---

### $\text{Slope}_{\theta_1}$

$$\frac{d}{d\theta_1} J(\theta_0, \theta_1) = \frac{d}{d\theta_1} \left( \frac{1}{2m} \sum_{i=1}^{m} \left( \theta_0 + \theta_1 x^i - y^i \right)^2 \right)$$

$$= \frac{1}{\cancel{2}m} \times \cancel{2} \sum_{i=1}^{m} (\theta_0 + \theta_1 x^i - y^i)(x^i)$$

$$\frac{d}{d\theta_1} J(\theta_0, \theta_1) = \frac{1}{m} \sum_{i=1}^{m} (\theta_0 + \theta_1 x^i - y^i) \times x^i$$

---

# Generally:

$$\frac{d}{d\theta_j} J(\theta_0, \dots, \theta_n) = \frac{1}{m} \sum_{i=1}^{m} (\theta_0 + \theta_j x^i - y^i) \times x_j^i$$