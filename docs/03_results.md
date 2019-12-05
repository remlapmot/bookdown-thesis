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

<table class="table" style="margin-left: auto; margin-right: auto;">
<caption>(\#tab:mtreg)Parameter estimates from regression of mpg on weight.</caption>
 <thead>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> Estimate </th>
   <th style="text-align:right;"> 95% CI lower limit </th>
   <th style="text-align:right;"> 95% CI upper limit </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> (Intercept) </td>
   <td style="text-align:right;"> 37.29 </td>
   <td style="text-align:right;"> 33.61 </td>
   <td style="text-align:right;"> 40.97 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> wt </td>
   <td style="text-align:right;"> -5.34 </td>
   <td style="text-align:right;"> -6.44 </td>
   <td style="text-align:right;"> -4.25 </td>
  </tr>
</tbody>
</table>

Example text example text example text example text example text example text example text example text example text example text example text example text example text example text example text example text example text example text.

An example of a figure is shown in Figure \@ref(fig:pressure).

```r
plot(pressure, pch = 19, type = "b")
```

<div class="figure" style="text-align: center">
<img src="03_results_files/figure-html/pressure-1.png" alt="An example figure." width="75%" />
<p class="caption">(\#fig:pressure)An example figure.</p>
</div>

And we can include image files directly, such as Figure \@ref(fig:knitlogo).

```r
knitr::include_graphics("img/mtcars-scatter.png")
```

<div class="figure" style="text-align: center">
<img src="img/mtcars-scatter.png" alt="Another example figure." width="75%" />
<p class="caption">(\#fig:knitlogo)Another example figure.</p>
</div>

To figure code chunks add the chunk option `fig.pos="H"` to use the LaTeX float package to try and position the figure where the code appears.

Also, this is how to reference a section, e.g. the Introduction was chapter \@ref(introduction) and the Literature Review was section \@ref(literature-review).
