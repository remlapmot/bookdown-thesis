# Results




## Main results

And here is an example table of regression coefficients in Table \@ref(tab:mtreg).


```r
mod <- lm(mpg ~ wt, data = mtcars)
coefcis <- cbind(coef(mod), confint.default(mod))
colnames(coefcis) <-
  c("Estimate", "95% CI lower limit", "95% CI upper limit")
knitr::kable(coefcis,
             digits = 2,
             booktabs = TRUE,
             caption = "Parameter estimates from regression of mpg on weight.") %>%
  kable_styling(latex_options = c("HOLD_position"))
```

\begin{table}[H]

\caption{(\#tab:mtreg)Parameter estimates from regression of mpg on weight.}
\centering
\begin{tabular}[t]{lrrr}
\toprule
  & Estimate & 95\% CI lower limit & 95\% CI upper limit\\
\midrule
(Intercept) & 37.29 & 33.61 & 40.97\\
wt & -5.34 & -6.44 & -4.25\\
\bottomrule
\end{tabular}
\end{table}

Example text example text example text example text example text example text example text example text example text example text example text example text example text example text example text example text example text example text.

An example of a figure is shown in Figure \@ref(fig:pressure).

```r
plot(pressure, pch = 19, type = "b")
```

\begin{figure}[H]

{\centering \includegraphics[width=0.75\linewidth]{03_results_files/figure-latex/pressure-1} 

}

\caption{An example figure.}(\#fig:pressure)
\end{figure}

And we can include image files directly, such as Figure \@ref(fig:knitlogo).

```r
knitr::include_graphics("img/mtcars-scatter.png")
```

\begin{figure}

{\centering \includegraphics[width=0.75\linewidth]{img/mtcars-scatter} 

}

\caption{Another example figure.}(\#fig:knitlogo)
\end{figure}

To figure code chunks add the chunk option `fig.pos="H"` to use the LaTeX float package to try and position the figure where the code appears.

Also, this is how to reference a section, e.g. the Introduction was chapter \@ref(introduction) and the Literature Review was section \@ref(literature-review).
