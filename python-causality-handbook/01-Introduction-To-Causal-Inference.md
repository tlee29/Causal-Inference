### _01 Introduction To Causal Inference_</br></br>

`Treatment (T)`
```
Ti(0) = Individual i did not receive the treatment
Ti(1) = Individual i received the treatment
```

`Potential Outcome (Y)`
```
Yi(0) = Y0i = Potential outcome for unit i without the treatment
Yi(1) = Y1i = Potential outcome for the same unit i with the treatment
```
</br>

***Factual and Counterfactual Graph***</br>
>In the case where individual `i` is not treated, $`T0_i`$, the factual outcome would be $`Y0_i`$ whilst counterfactual outcome is $`Y1_i`$

```mermaid
flowchart LR
    A(Ti)-->B(0);
    A --> C(1);
    B --- D1@{ shape: stadium, label: "factual"} --> D(Y0i)
    B --- D2@{ shape: stadium, label: "counterfactual"} --> E(Y1i)
    C --- F1@{ shape: stadium, label: "factual"} --> F(Y1i)
    C --- F2@{ shape: stadium, label: "counterfactual"}--> G(Y0i)
    D1:::foo & D:::foo
    F1:::foo & F:::foo
    classDef foo stroke:#f00
    
```
>[!Note]
><sup>Counterfactual can't coexist with the factual event and be explicitly observed since the same individual `i` should be treated under the same condition (=Impossible)</sup>
