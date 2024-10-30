# 5주차 강의 요약  

![image](https://github.com/user-attachments/assets/a7f9f1d4-108b-4a22-b004-a480052bb04e)   

State Variables의 개념은 시스템을 먼저 states를 정의하고 의미를 주어 문제를 푸는 것이다.  사람이 보기 편하고 컴퓨터에게 문제를 풀기 쉽게 만들어주는 것이다.    

   
![image](https://github.com/user-attachments/assets/e2ebf50f-2256-4685-bf79-c9a136aa9eda)

$$M\frac{\partial^2 y(t)}{\partial t^2} + b\frac{\partial y(t)}{\partial t} + ky(t) = r(t)$$
$$x_{1}(t)=y(t), x_{2}(t)=\frac{\partial y(t)}{\partial t}$$
$$\frac{\partial x_{1}(t)}{\partial t} = x_{2}(t)$$
$$\frac{\partial x_{2}(t)}{\partial t} = \frac{-b}{M}x_{2}(t)-\frac{-k}{M}x_{1}(t)+\frac{1}{M}r(t)$$

와 같이 연립방정식형태로 변형할수 있다.    
연립방정식으로 만들면 결국 1차 미분방정식과 연립이 행렬이기 때문에 행렬기준으로는 컴퓨터는 1차 미분방정식으로 처리하기 때문에 매우 효율적이다.

State Space Equation 의 기본 형태는 다음과 같다   
$$x(t)=\Phi(t)\cdot x(0)+\int \Phi (t-\tau)bu(\tau)dt$$

적분 밖에 있는 식과 적분 안에있는 식이 나오게된다.
왼쪽 식은 x(0)는 초기 값이기에 초기값에 파이(t)르 곱한 형식이 된다.
오른쪽 식은 인풋에 파이 값을 곱한 형식이 나오게된다.
