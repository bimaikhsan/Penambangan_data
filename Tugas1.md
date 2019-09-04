

```python
import pandas as pd
from scipy import stats
df = pd.read_csv('Data.csv',sep=';')
data = {"stats": ['Min','Max','Mean','Standard Deviasi','Variasi','Skewnes','Quantile 1','Quantile 2',
                  'Quantile 3','Median','Modus']}
for i in df.columns:
    data[i] = [df[i].min(), df[i].max(), df[i].mean(), round(df[i].std(),2), round(df[i].var(),2),
               round(df[i].skew(),2), df[i].quantile(0.25),df[i].quantile(0.5),df[i].quantile(0.75), 
               df[i].median(), stats.mode(df[i]).mode[0]]
tes = pd.DataFrame(data,columns = ['stats'] + [x for x in df.columns])
tes.style.hide_index()
```




<style  type="text/css" >
</style><table id="T_4a22305c_cf30_11e9_a68e_b0fc3661437a" ><thead>    <tr>        <th class="col_heading level0 col0" >stats</th>        <th class="col_heading level0 col1" >data 1</th>        <th class="col_heading level0 col2" >data 2</th>        <th class="col_heading level0 col3" >data 3</th>        <th class="col_heading level0 col4" >data 4</th>    </tr></thead><tbody>
                <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow0_col0" class="data row0 col0" >Min</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow0_col1" class="data row0 col1" >81</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow0_col2" class="data row0 col2" >81</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow0_col3" class="data row0 col3" >80</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow0_col4" class="data row0 col4" >80</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow1_col0" class="data row1 col0" >Max</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow1_col1" class="data row1 col1" >160</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow1_col2" class="data row1 col2" >160</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow1_col3" class="data row1 col3" >160</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow1_col4" class="data row1 col4" >160</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow2_col0" class="data row2 col0" >Mean</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow2_col1" class="data row2 col1" >120.26</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow2_col2" class="data row2 col2" >124.67</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow2_col3" class="data row2 col3" >122</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow2_col4" class="data row2 col4" >118.02</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow3_col0" class="data row3 col0" >Standard Deviasi</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow3_col1" class="data row3 col1" >24.78</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow3_col2" class="data row3 col2" >22.47</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow3_col3" class="data row3 col3" >24.55</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow3_col4" class="data row3 col4" >22.67</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow4_col0" class="data row4 col0" >Variasi</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow4_col1" class="data row4 col1" >613.89</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow4_col2" class="data row4 col2" >504.89</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow4_col3" class="data row4 col3" >602.57</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow4_col4" class="data row4 col4" >513.72</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow5_col0" class="data row5 col0" >Skewnes</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow5_col1" class="data row5 col1" >0.11</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow5_col2" class="data row5 col2" >-0.22</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow5_col3" class="data row5 col3" >-0.07</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow5_col4" class="data row5 col4" >0.12</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow6_col0" class="data row6 col0" >Quartile 1</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow6_col1" class="data row6 col1" >97</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow6_col2" class="data row6 col2" >106.75</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow6_col3" class="data row6 col3" >101.75</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow6_col4" class="data row6 col4" >99.5</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow7_col0" class="data row7 col0" >Quartile 2</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow7_col1" class="data row7 col1" >117.5</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow7_col2" class="data row7 col2" >126.5</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow7_col3" class="data row7 col3" >123.5</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow7_col4" class="data row7 col4" >118</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow8_col0" class="data row8 col0" >Quartile 3</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow8_col1" class="data row8 col1" >143.25</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow8_col2" class="data row8 col2" >143.25</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow8_col3" class="data row8 col3" >144</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow8_col4" class="data row8 col4" >137.25</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow9_col0" class="data row9 col0" >Median</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow9_col1" class="data row9 col1" >117.5</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow9_col2" class="data row9 col2" >126.5</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow9_col3" class="data row9 col3" >123.5</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow9_col4" class="data row9 col4" >118</td>
            </tr>
            <tr>
                                <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow10_col0" class="data row10 col0" >Modus</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow10_col1" class="data row10 col1" >84</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow10_col2" class="data row10 col2" >131</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow10_col3" class="data row10 col3" >89</td>
                        <td id="T_4a22305c_cf30_11e9_a68e_b0fc3661437arow10_col4" class="data row10 col4" >124</td>
            </tr>
    </tbody></table>




```python

```
