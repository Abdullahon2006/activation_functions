# Neural Network Activation Functions

A Java implementation of fundamental activation functions used in artificial neural networks.

## **Implemented Functions**

1. **Heaviside Step Function**
   ```
   H(x) = { 0 if x < 0
            0.5 if x = 0
            1 if x > 0 }
   ```

2. **Sigmoid Function**
   ```
   σ(x) = 1 / (1 + e^-x)
   ```

3. **Hyperbolic Tangent**
   ```
   tanh(x) = (e^x - e^-x) / (e^x + e^-x)
   ```

4. **Softsign Function**
   ```
   f(x) = x / (1 + |x|)
   ```

5. **Square Nonlinearity (SQNL)**
   ```
   SQNL(x) = { -1 if x ≤ -2
               x + x²/4 if -2 < x < 0
               x - x²/4 if 0 ≤ x < 2
               1 if x ≥ 2 }
   ```

## **Usage**

1. **Compile** the program:
   ```bash
   javac ActivationFunction.java
   ```

2. **Run** with a double argument:
   ```bash
   java ActivationFunction x
   ```
   Where `x` is the input value to evaluate

## **Examples**

```bash
$ java ActivationFunction 0.5
heaviside(0.5) = 1.0
  sigmoid(0.5) = 0.6224593312018546
     tanh(0.5) = 0.4621171572600098
 softsign(0.5) = 0.3333333333333333
     sqnl(0.5) = 0.4375

$ java ActivationFunction -1.2
heaviside(-1.2) = 0.0
  sigmoid(-1.2) = 0.23147521650098238
     tanh(-1.2) = -0.8336546070121552
 softsign(-1.2) = -0.5454545454545454
     sqnl(-1.2) = -0.66
```

## **Technical Specifications**
- All functions return `Double.NaN` for NaN inputs
- Uses standard `Math` library for exponential and absolute value operations
- Output formatted to show full double precision
- Piecewise functions implemented with exact boundary conditions

## **Applications**
- Neural network development
- Machine learning research
- Activation function comparison studies
- Educational demonstrations of neural network mathematics
