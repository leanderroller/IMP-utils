# plotting examples

Some examples of the [plotting command set](plotting.md) to help you understand it.

## errorbar plot

### only errorplot example

<p align="left">
  <img src="./images/plot_T4_V.png" width="400" title="only errorplot example" alt="only errorplot example">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/T4_V.csv"
ERRORBAR_PLOT_PATH = "data/graphics/plot_T4_V.png"
ERRORBAR_PLOT_X_COLUMN = 'V'
ERRORBAR_PLOT_X_ERROR_COLUMN = "u_V"
ERRORBAR_PLOT_Y_COLUMN = "p"
ERRORBAR_PLOT_Y_ERROR_COLUMN = "u_p"
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = "Druck p in Bar"
ERRORBAR_PLOT_YLABEL = "Volumen V in $cm^3$"
ERRORBAR_PLOT_XTICKS_NUMBER = 8
ERRORBAR_PLOT_MIN_XTICKS = 0
ERRORBAR_PLOT_MAX_XTICKS = "auto"
ERRORBAR_PLOT_PLOTLABELS = ""
ERRORBAR_PLOT_MODEL = "none"
ERRORBAR_PLOT_SHOW_MODELERROR = False
ERRORBAR_PLOT_EXTRA_LOG = False
```
</details>

### O11 plot example

<p align="left">
  <img src="./images/plot_O11.png" width="400" title="O11 plot example" alt="O11 plot example">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/O11_data.csv"
ERRORBAR_PLOT_PATH = "data/graphics/plot_O11.png"
ERRORBAR_PLOT_X_COLUMN = ["a_parallel", "a_orth"]
ERRORBAR_PLOT_X_ERROR_COLUMN = ["u_a_parallel", "u_a_orth"]
ERRORBAR_PLOT_Y_COLUMN = ["R_parallel", "R_orth"]
ERRORBAR_PLOT_Y_ERROR_COLUMN = ["u_R_parallel", "u_R_orth"]
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = r"Winkel $\alpha$ in Grad"
ERRORBAR_PLOT_YLABEL = r"Wurzel des Reflexionskoeffizienten $\sqrt{R}$"
ERRORBAR_PLOT_XTICKS_NUMBER = 17
ERRORBAR_PLOT_MIN_XTICKS = "auto"
ERRORBAR_PLOT_MAX_XTICKS = "auto"
ERRORBAR_PLOT_PLOTLABELS = [r"$\sqrt{R_p}$", r"$\sqrt{R_s}$"]
ERRORBAR_PLOT_MODEL = ["O11_Rp", "O11_Rs"]
ERRORBAR_PLOT_SHOW_MODELERROR = False
ERRORBAR_PLOT_EXTRA_LOG = False
```
</details>

with command (replace the gin_param values with your n1 and n2 values (Brechungsindizes), here: 1 and 1.5):
```
python IMP_utils_py/cli.py --mode=errorbar-plot --gin_file=IMP_utils_py/config/plotting.gin --gin_param O11_Rs_Rp_model.n1=1 --gin_param O11_Rs_Rp_model.n2=1.5
```

### constant plot example

<p align="left">
  <img src="./images/plot_T4_pV_korr.png" width="400" title="constant plot example" alt="constant plot example">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/T4_V.csv"
ERRORBAR_PLOT_PATH = "data/graphics/plot_T4_pV_korr.png"
ERRORBAR_PLOT_X_COLUMN = 'V_korr'
ERRORBAR_PLOT_X_ERROR_COLUMN = "u_V_korr"
ERRORBAR_PLOT_Y_COLUMN = "pV_korr"
ERRORBAR_PLOT_Y_ERROR_COLUMN = "u_pV_korr"
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = "korrigierte Volumen $V_{korr}$ in $cm^3$"
ERRORBAR_PLOT_YLABEL = "korrigierter Volumen-Druck $pV_{korr}$ in Bar$\cdot cm^3$"
ERRORBAR_PLOT_XTICKS_NUMBER = 8
ERRORBAR_PLOT_MIN_XTICKS = 0
ERRORBAR_PLOT_MAX_XTICKS = "auto"
ERRORBAR_PLOT_PLOTLABELS = ""
ERRORBAR_PLOT_MODEL = "constant"
ERRORBAR_PLOT_SHOW_MODELERROR = False
ERRORBAR_PLOT_EXTRA_LOG = False
```
</details>

### weighted_average plot with errorareas example

<p align="left">
  <img src="./images/plot_E1_wb.png" width="400" title="weighted_average plot with errorareas example" alt="weighted_average plot with errorareas example">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/E1_wb.csv"
ERRORBAR_PLOT_PATH = "data/graphics/plot_E1_wb.png"
ERRORBAR_PLOT_X_COLUMN = "R_N (R1)"
ERRORBAR_PLOT_X_ERROR_COLUMN = "u_R_N (R1)"
ERRORBAR_PLOT_Y_COLUMN = "R_1"
ERRORBAR_PLOT_Y_ERROR_COLUMN = "u_R_1"
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = "Widerstand R$_N$ in Ohm"
ERRORBAR_PLOT_YLABEL = "Widerstand R$_1$ in Ohm"
ERRORBAR_PLOT_XTICKS_NUMBER = "auto"
ERRORBAR_PLOT_MIN_XTICKS = "auto"
ERRORBAR_PLOT_MAX_XTICKS = "auto"
ERRORBAR_PLOT_PLOTLABELS = ""
ERRORBAR_PLOT_MODEL = "weighted_average"
ERRORBAR_PLOT_SHOW_MODELERROR = True
ERRORBAR_PLOT_EXTRA_LOG = False
```
</details>

### linear plot example

<p align="left">
  <img src="./images/plot_O6_bhg.png" width="400" title="linear plot example" alt="linear plot example">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/O6_bhg.csv"
ERRORBAR_PLOT_PATH = "data/graphics/plot_O6_bhg.png"
ERRORBAR_PLOT_X_COLUMN = 'k'
ERRORBAR_PLOT_X_ERROR_COLUMN = ""
ERRORBAR_PLOT_Y_COLUMN = "y"
ERRORBAR_PLOT_Y_ERROR_COLUMN = "uy"
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = "k"
ERRORBAR_PLOT_YLABEL = "$r_k^2$ in $mm^2$"
ERRORBAR_PLOT_XTICKS_NUMBER = "auto"
ERRORBAR_PLOT_MIN_XTICKS = 0
ERRORBAR_PLOT_MAX_XTICKS = "auto"
ERRORBAR_PLOT_PLOTLABELS = ""
ERRORBAR_PLOT_MODEL = "linear"
ERRORBAR_PLOT_SHOW_MODELERROR = False
ERRORBAR_PLOT_EXTRA_LOG = False
```
</details>

### multiple all linear plots example 1

<p align="left">
  <img src="./images/plot_M12_kg.png" width="400" title="multiple all linear plots example 1" alt="multiple all linear plots example 1">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/M12_kg.csv"
ERRORBAR_PLOT_PATH = "data/graphics/plot_M12_kg.png"
ERRORBAR_PLOT_X_COLUMN = 'n'
ERRORBAR_PLOT_X_ERROR_COLUMN = ""
ERRORBAR_PLOT_Y_COLUMN = ["f_1kg", "f_2kg", "f_3kg"]
ERRORBAR_PLOT_Y_ERROR_COLUMN = ["u_1kg", "u_2kg", "u_3kg"]
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = "n"
ERRORBAR_PLOT_YLABEL = "Frequenzen $f_n$ in Hz für 1kg/2kg/3kg"
ERRORBAR_PLOT_XTICKS_NUMBER = 8
ERRORBAR_PLOT_MIN_XTICKS = 0
ERRORBAR_PLOT_MAX_XTICKS = "auto"
ERRORBAR_PLOT_PLOTLABELS = ["1kg", "2kg", "3kg"]
ERRORBAR_PLOT_MODEL = "linear"
ERRORBAR_PLOT_SHOW_MODELERROR = False
ERRORBAR_PLOT_EXTRA_LOG = False
```
</details>

### multiple all linear plots example 2

<p align="left">
  <img src="./images/plot_E1_UI.png" width="400" title="multiple all linear plots example 2" alt="multiple all linear plots example 2">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/E1_UI.csv"
ERRORBAR_PLOT_PATH = "data/graphics/plot_E1_UI.png"
ERRORBAR_PLOT_X_COLUMN = ["I_1", "I_2"]
ERRORBAR_PLOT_X_ERROR_COLUMN = ["u_I_1", "u_I_2"]
ERRORBAR_PLOT_Y_COLUMN = ["U_1", "U_2"]
ERRORBAR_PLOT_Y_ERROR_COLUMN = ["u_U_1", "u_U_2"]
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = "Stromstärke I in A"
ERRORBAR_PLOT_YLABEL = "Spannung U in V"
ERRORBAR_PLOT_XTICKS_NUMBER = "auto"
ERRORBAR_PLOT_MIN_XTICKS = 0
ERRORBAR_PLOT_MAX_XTICKS = 0.2
ERRORBAR_PLOT_PLOTLABELS = ["Stromfehlerschaltung", "Spannungsfehlerschaltung"]
ERRORBAR_PLOT_MODEL = "linear"
ERRORBAR_PLOT_SHOW_MODELERROR = False
ERRORBAR_PLOT_EXTRA_LOG = False
```
</details>

### multiple all linear_zero plots example

<p align="left">
  <img src="./images/plot_E12_e.png" width="400" title="multiple all linear_zero plots example" alt="multiple all linear_zero plots example">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/E12_e.csv"
ERRORBAR_PLOT_PATH = "data/graphics/plot_E12_e.png"
ERRORBAR_PLOT_X_COLUMN = ["r_3000", "r_4000", "r_5000"]
ERRORBAR_PLOT_X_ERROR_COLUMN = ["u_r_3000", "u_r_4000", "u_r_5000"]
ERRORBAR_PLOT_Y_COLUMN = ["1/B_3000", "1/B_4000", "1/B_5000"]
ERRORBAR_PLOT_Y_ERROR_COLUMN = ["u_1/B_3000", "u_1/B_4000", "u_1/B_5000"]
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = "Bahnradius der Elektronen $r$ in m"
ERRORBAR_PLOT_YLABEL = "reziproke magnetischen Flussdichte $1/B$ in $1/T$"
ERRORBAR_PLOT_XTICKS_NUMBER = "auto"
ERRORBAR_PLOT_MIN_XTICKS = 0
ERRORBAR_PLOT_MAX_XTICKS = "auto"
ERRORBAR_PLOT_PLOTLABELS = ["$U_A = 3000 V$", "$U_A = 4000 V$", "$U_A = 5000 V$"]
ERRORBAR_PLOT_MODEL = "linear_zero"
ERRORBAR_PLOT_SHOW_MODELERROR = False
ERRORBAR_PLOT_EXTRA_LOG = False
```
</details>

### multiple linear/none plots example

<p align="left">
  <img src="./images/plot_E5_UI.png" width="400" title="multiple linear/none plots example" alt="multiple linear/none plots example">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/E5_UI.csv"
ERRORBAR_PLOT_PATH = "data/graphics/plot_E5_UI.png"
ERRORBAR_PLOT_X_COLUMN = ["I_EoK", "I_EmK", "I_ZoK", "I_ZmK"]
ERRORBAR_PLOT_X_ERROR_COLUMN = ["u_I_EoK", "u_I_EmK", "u_I_ZoK", "u_I_ZmK"]
ERRORBAR_PLOT_Y_COLUMN = ["U_EoK", "U_EmK", "U_ZoK", "U_ZmK"]
ERRORBAR_PLOT_Y_ERROR_COLUMN = ["u_U_EoK", "u_U_EmK", "u_U_ZoK", "u_U_ZmK"]
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = "Stromstärke I in mA"
ERRORBAR_PLOT_YLABEL = "Spannung U in V"
ERRORBAR_PLOT_XTICKS_NUMBER = 11
ERRORBAR_PLOT_MIN_XTICKS = 0
ERRORBAR_PLOT_MAX_XTICKS = 125
ERRORBAR_PLOT_PLOTLABELS = ["EWG ohne Kondensator", "EWG mit Kondensator", "ZWG ohne Kondensator", "ZWG mit Kondensator"]
ERRORBAR_PLOT_MODEL = ["linear", "none", "linear", "none"]
ERRORBAR_PLOT_SHOW_MODELERROR = False
ERRORBAR_PLOT_EXTRA_LOG = True
```
</details>

## residual plot

### example plot

<p align="left">
  <img src="./images/plot_O6_bhg_residual.png" width="400" title="residual plot example" alt="residual plot example">
</p>

<details><summary>parameters</summary>

``` // opening
RAW_DATA_PATH = "data/Grundpraktikum/O6_bhg.csv"
RESIDUAL_PLOT_PATH = "data/graphics/plot_O6_bhg_residual.png"
ERRORBAR_PLOT_X_COLUMN = 'k'
ERRORBAR_PLOT_X_ERROR_COLUMN = ""
ERRORBAR_PLOT_Y_COLUMN = "y"
ERRORBAR_PLOT_Y_ERROR_COLUMN = "uy"
ERRORBAR_PLOT_TITLE = ""
ERRORBAR_PLOT_XLABEL = "k"
ERRORBAR_PLOT_YLABEL = "$r_k^2$ in $mm^2$"
ERRORBAR_PLOT_XTICKS_NUMBER = "auto"
ERRORBAR_PLOT_MIN_XTICKS = 0
ERRORBAR_PLOT_MAX_XTICKS = "auto"
ERRORBAR_PLOT_MODEL = "linear"
```
</details>
