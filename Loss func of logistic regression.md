### Cost function
$\hat{y} = \sigma(w^Tx+b)$ is predict value

$y=1$ or $y=0$ is real value

because of $\sigma(z)=1/(1+e^{-z})$, which means that $\hat{y}\in(0,1)$ and $\hat{y}=0.5$ if $z=0$, just as probability

we can interpret as: $\hat{y}=P(y=1\mid x)$

if $y=1, P(y\mid x)=\hat{y}$

if $y=0, P(y\mid x)=1-\hat{y}$
          
together, $P(y\mid x)=\hat{y}^{y}+(1-\hat{y})^{1-y}$

Because that log() is strictly monotonically increasing function, then maximize $P(y\mid x)$ is equal to 
minimize $-log(P(y\mid x))=-[ylog\hat{y}+(1-y)log(1-\hat{y})]$

but why maximize $P(y\mid x)$ (lost func), may be for maximize likelyhood
