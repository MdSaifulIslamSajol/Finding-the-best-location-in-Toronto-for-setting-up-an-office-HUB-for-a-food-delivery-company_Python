```python
import numpy as np
import pandas as pd

```


```python
!pip install html5lib
import html5lib
```

    Requirement already satisfied: html5lib in c:\users\saifu\anaconda3\lib\site-packages (1.0.1)
    Requirement already satisfied: webencodings in c:\users\saifu\anaconda3\lib\site-packages (from html5lib) (0.5.1)
    Requirement already satisfied: six>=1.9 in c:\users\saifu\anaconda3\lib\site-packages (from html5lib) (1.12.0)
    

Importing Data from Wikipedia


```python
uss=pd.read_html('https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M')
```


```python
print(type(uss))
```

    <class 'list'>
    


```python
uss[0].head(34)
my_dataframe=uss[0]
my_dataframe
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postcode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>M1A</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>1</td>
      <td>M2A</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>2</td>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
    </tr>
    <tr>
      <td>3</td>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
    </tr>
    <tr>
      <td>4</td>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront</td>
    </tr>
    <tr>
      <td>5</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Heights</td>
    </tr>
    <tr>
      <td>6</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Manor</td>
    </tr>
    <tr>
      <td>7</td>
      <td>M7A</td>
      <td>Queen's Park</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>8</td>
      <td>M8A</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>9</td>
      <td>M9A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park</td>
    </tr>
    <tr>
      <td>10</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge</td>
    </tr>
    <tr>
      <td>11</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Malvern</td>
    </tr>
    <tr>
      <td>12</td>
      <td>M2B</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>13</td>
      <td>M3B</td>
      <td>North York</td>
      <td>Don Mills North</td>
    </tr>
    <tr>
      <td>14</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Woodbine Gardens</td>
    </tr>
    <tr>
      <td>15</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Parkview Hill</td>
    </tr>
    <tr>
      <td>16</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Ryerson</td>
    </tr>
    <tr>
      <td>17</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Garden District</td>
    </tr>
    <tr>
      <td>18</td>
      <td>M6B</td>
      <td>North York</td>
      <td>Glencairn</td>
    </tr>
    <tr>
      <td>19</td>
      <td>M7B</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>20</td>
      <td>M8B</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>21</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Cloverdale</td>
    </tr>
    <tr>
      <td>22</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Islington</td>
    </tr>
    <tr>
      <td>23</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Martin Grove</td>
    </tr>
    <tr>
      <td>24</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Princess Gardens</td>
    </tr>
    <tr>
      <td>25</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>West Deane Park</td>
    </tr>
    <tr>
      <td>26</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek</td>
    </tr>
    <tr>
      <td>27</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Rouge Hill</td>
    </tr>
    <tr>
      <td>28</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Port Union</td>
    </tr>
    <tr>
      <td>29</td>
      <td>M2C</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>30</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Flemingdon Park</td>
    </tr>
    <tr>
      <td>31</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Don Mills South</td>
    </tr>
    <tr>
      <td>32</td>
      <td>M4C</td>
      <td>East York</td>
      <td>Woodbine Heights</td>
    </tr>
    <tr>
      <td>33</td>
      <td>M5C</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
    </tr>
    <tr>
      <td>34</td>
      <td>M6C</td>
      <td>York</td>
      <td>Humewood-Cedarvale</td>
    </tr>
    <tr>
      <td>35</td>
      <td>M7C</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>36</td>
      <td>M8C</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>37</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Bloordale Gardens</td>
    </tr>
    <tr>
      <td>38</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Eringate</td>
    </tr>
    <tr>
      <td>39</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Markland Wood</td>
    </tr>
    <tr>
      <td>40</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Old Burnhamthorpe</td>
    </tr>
    <tr>
      <td>41</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood</td>
    </tr>
    <tr>
      <td>42</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Morningside</td>
    </tr>
    <tr>
      <td>43</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>West Hill</td>
    </tr>
    <tr>
      <td>44</td>
      <td>M2E</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>45</td>
      <td>M3E</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>46</td>
      <td>M4E</td>
      <td>East Toronto</td>
      <td>The Beaches</td>
    </tr>
    <tr>
      <td>47</td>
      <td>M5E</td>
      <td>Downtown Toronto</td>
      <td>Berczy Park</td>
    </tr>
    <tr>
      <td>48</td>
      <td>M6E</td>
      <td>York</td>
      <td>Caledonia-Fairbanks</td>
    </tr>
    <tr>
      <td>49</td>
      <td>M7E</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>50</td>
      <td>M8E</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>51</td>
      <td>M9E</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>52</td>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <td>53</td>
      <td>M2G</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>54</td>
      <td>M3G</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>55</td>
      <td>M4G</td>
      <td>East York</td>
      <td>Leaside</td>
    </tr>
    <tr>
      <td>56</td>
      <td>M5G</td>
      <td>Downtown Toronto</td>
      <td>Central Bay Street</td>
    </tr>
    <tr>
      <td>57</td>
      <td>M6G</td>
      <td>Downtown Toronto</td>
      <td>Christie</td>
    </tr>
    <tr>
      <td>58</td>
      <td>M7G</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>59</td>
      <td>M8G</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>60</td>
      <td>M9G</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>61</td>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
    <tr>
      <td>62</td>
      <td>M2H</td>
      <td>North York</td>
      <td>Hillcrest Village</td>
    </tr>
    <tr>
      <td>63</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Bathurst Manor</td>
    </tr>
    <tr>
      <td>64</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Downsview North</td>
    </tr>
    <tr>
      <td>65</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Wilson Heights</td>
    </tr>
    <tr>
      <td>66</td>
      <td>M4H</td>
      <td>East York</td>
      <td>Thorncliffe Park</td>
    </tr>
    <tr>
      <td>67</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Adelaide</td>
    </tr>
    <tr>
      <td>68</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>King</td>
    </tr>
    <tr>
      <td>69</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Richmond</td>
    </tr>
    <tr>
      <td>70</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dovercourt Village</td>
    </tr>
    <tr>
      <td>71</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dufferin</td>
    </tr>
    <tr>
      <td>72</td>
      <td>M7H</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>73</td>
      <td>M8H</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>74</td>
      <td>M9H</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>75</td>
      <td>M1J</td>
      <td>Scarborough</td>
      <td>Scarborough Village</td>
    </tr>
    <tr>
      <td>76</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Fairview</td>
    </tr>
    <tr>
      <td>77</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Henry Farm</td>
    </tr>
    <tr>
      <td>78</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Oriole</td>
    </tr>
    <tr>
      <td>79</td>
      <td>M3J</td>
      <td>North York</td>
      <td>Northwood Park</td>
    </tr>
    <tr>
      <td>80</td>
      <td>M3J</td>
      <td>North York</td>
      <td>York University</td>
    </tr>
    <tr>
      <td>81</td>
      <td>M4J</td>
      <td>East York</td>
      <td>East Toronto</td>
    </tr>
    <tr>
      <td>82</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront East</td>
    </tr>
    <tr>
      <td>83</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Toronto Islands</td>
    </tr>
    <tr>
      <td>84</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Union Station</td>
    </tr>
    <tr>
      <td>85</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Little Portugal</td>
    </tr>
    <tr>
      <td>86</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Trinity</td>
    </tr>
    <tr>
      <td>87</td>
      <td>M7J</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>88</td>
      <td>M8J</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>89</td>
      <td>M9J</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>90</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>East Birchmount Park</td>
    </tr>
    <tr>
      <td>91</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>Ionview</td>
    </tr>
    <tr>
      <td>92</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>Kennedy Park</td>
    </tr>
    <tr>
      <td>93</td>
      <td>M2K</td>
      <td>North York</td>
      <td>Bayview Village</td>
    </tr>
    <tr>
      <td>94</td>
      <td>M3K</td>
      <td>North York</td>
      <td>CFB Toronto</td>
    </tr>
    <tr>
      <td>95</td>
      <td>M3K</td>
      <td>North York</td>
      <td>Downsview East</td>
    </tr>
    <tr>
      <td>96</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>The Danforth West</td>
    </tr>
    <tr>
      <td>97</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>Riverdale</td>
    </tr>
    <tr>
      <td>98</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Design Exchange</td>
    </tr>
    <tr>
      <td>99</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Toronto Dominion Centre</td>
    </tr>
    <tr>
      <td>100</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Brockton</td>
    </tr>
    <tr>
      <td>101</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Exhibition Place</td>
    </tr>
    <tr>
      <td>102</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Parkdale Village</td>
    </tr>
    <tr>
      <td>103</td>
      <td>M7K</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>104</td>
      <td>M8K</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>105</td>
      <td>M9K</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>106</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Clairlea</td>
    </tr>
    <tr>
      <td>107</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Golden Mile</td>
    </tr>
    <tr>
      <td>108</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Oakridge</td>
    </tr>
    <tr>
      <td>109</td>
      <td>M2L</td>
      <td>North York</td>
      <td>Silver Hills</td>
    </tr>
    <tr>
      <td>110</td>
      <td>M2L</td>
      <td>North York</td>
      <td>York Mills</td>
    </tr>
    <tr>
      <td>111</td>
      <td>M3L</td>
      <td>North York</td>
      <td>Downsview West</td>
    </tr>
    <tr>
      <td>112</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>The Beaches West</td>
    </tr>
    <tr>
      <td>113</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>India Bazaar</td>
    </tr>
    <tr>
      <td>114</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Commerce Court</td>
    </tr>
    <tr>
      <td>115</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Victoria Hotel</td>
    </tr>
    <tr>
      <td>116</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Downsview</td>
    </tr>
    <tr>
      <td>117</td>
      <td>M6L</td>
      <td>North York</td>
      <td>North Park</td>
    </tr>
    <tr>
      <td>118</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Upwood Park</td>
    </tr>
    <tr>
      <td>119</td>
      <td>M7L</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>120</td>
      <td>M8L</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>121</td>
      <td>M9L</td>
      <td>North York</td>
      <td>Humber Summit</td>
    </tr>
    <tr>
      <td>122</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffcrest</td>
    </tr>
    <tr>
      <td>123</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffside</td>
    </tr>
    <tr>
      <td>124</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Scarborough Village West</td>
    </tr>
    <tr>
      <td>125</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Newtonbrook</td>
    </tr>
    <tr>
      <td>126</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Willowdale</td>
    </tr>
    <tr>
      <td>127</td>
      <td>M3M</td>
      <td>North York</td>
      <td>Downsview Central</td>
    </tr>
    <tr>
      <td>128</td>
      <td>M4M</td>
      <td>East Toronto</td>
      <td>Studio District</td>
    </tr>
    <tr>
      <td>129</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Bedford Park</td>
    </tr>
    <tr>
      <td>130</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Lawrence Manor East</td>
    </tr>
    <tr>
      <td>131</td>
      <td>M6M</td>
      <td>York</td>
      <td>Del Ray</td>
    </tr>
    <tr>
      <td>132</td>
      <td>M6M</td>
      <td>York</td>
      <td>Keelesdale</td>
    </tr>
    <tr>
      <td>133</td>
      <td>M6M</td>
      <td>York</td>
      <td>Mount Dennis</td>
    </tr>
    <tr>
      <td>134</td>
      <td>M6M</td>
      <td>York</td>
      <td>Silverthorn</td>
    </tr>
    <tr>
      <td>135</td>
      <td>M7M</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>136</td>
      <td>M8M</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>137</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Emery</td>
    </tr>
    <tr>
      <td>138</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Humberlea</td>
    </tr>
    <tr>
      <td>139</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Birch Cliff</td>
    </tr>
    <tr>
      <td>140</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Cliffside West</td>
    </tr>
    <tr>
      <td>141</td>
      <td>M2N</td>
      <td>North York</td>
      <td>Willowdale South</td>
    </tr>
    <tr>
      <td>142</td>
      <td>M3N</td>
      <td>North York</td>
      <td>Downsview Northwest</td>
    </tr>
    <tr>
      <td>143</td>
      <td>M4N</td>
      <td>Central Toronto</td>
      <td>Lawrence Park</td>
    </tr>
    <tr>
      <td>144</td>
      <td>M5N</td>
      <td>Central Toronto</td>
      <td>Roselawn</td>
    </tr>
    <tr>
      <td>145</td>
      <td>M6N</td>
      <td>York</td>
      <td>The Junction North</td>
    </tr>
    <tr>
      <td>146</td>
      <td>M6N</td>
      <td>York</td>
      <td>Runnymede</td>
    </tr>
    <tr>
      <td>147</td>
      <td>M7N</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>148</td>
      <td>M8N</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>149</td>
      <td>M9N</td>
      <td>York</td>
      <td>Weston</td>
    </tr>
    <tr>
      <td>150</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Dorset Park</td>
    </tr>
    <tr>
      <td>151</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Scarborough Town Centre</td>
    </tr>
    <tr>
      <td>152</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Wexford Heights</td>
    </tr>
    <tr>
      <td>153</td>
      <td>M2P</td>
      <td>North York</td>
      <td>York Mills West</td>
    </tr>
    <tr>
      <td>154</td>
      <td>M3P</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>155</td>
      <td>M4P</td>
      <td>Central Toronto</td>
      <td>Davisville North</td>
    </tr>
    <tr>
      <td>156</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill North</td>
    </tr>
    <tr>
      <td>157</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill West</td>
    </tr>
    <tr>
      <td>158</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>High Park</td>
    </tr>
    <tr>
      <td>159</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>The Junction South</td>
    </tr>
    <tr>
      <td>160</td>
      <td>M7P</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>161</td>
      <td>M8P</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>162</td>
      <td>M9P</td>
      <td>Etobicoke</td>
      <td>Westmount</td>
    </tr>
    <tr>
      <td>163</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Maryvale</td>
    </tr>
    <tr>
      <td>164</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Wexford</td>
    </tr>
    <tr>
      <td>165</td>
      <td>M2R</td>
      <td>North York</td>
      <td>Willowdale West</td>
    </tr>
    <tr>
      <td>166</td>
      <td>M3R</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>167</td>
      <td>M4R</td>
      <td>Central Toronto</td>
      <td>North Toronto West</td>
    </tr>
    <tr>
      <td>168</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>The Annex</td>
    </tr>
    <tr>
      <td>169</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>North Midtown</td>
    </tr>
    <tr>
      <td>170</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>Yorkville</td>
    </tr>
    <tr>
      <td>171</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Parkdale</td>
    </tr>
    <tr>
      <td>172</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Roncesvalles</td>
    </tr>
    <tr>
      <td>173</td>
      <td>M7R</td>
      <td>Mississauga</td>
      <td>Canada Post Gateway Processing Centre</td>
    </tr>
    <tr>
      <td>174</td>
      <td>M8R</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>175</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Kingsview Village</td>
    </tr>
    <tr>
      <td>176</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Martin Grove Gardens</td>
    </tr>
    <tr>
      <td>177</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Richview Gardens</td>
    </tr>
    <tr>
      <td>178</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>St. Phillips</td>
    </tr>
    <tr>
      <td>179</td>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
    </tr>
    <tr>
      <td>180</td>
      <td>M2S</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>181</td>
      <td>M3S</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>182</td>
      <td>M4S</td>
      <td>Central Toronto</td>
      <td>Davisville</td>
    </tr>
    <tr>
      <td>183</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>Harbord</td>
    </tr>
    <tr>
      <td>184</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>University of Toronto</td>
    </tr>
    <tr>
      <td>185</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Runnymede</td>
    </tr>
    <tr>
      <td>186</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Swansea</td>
    </tr>
    <tr>
      <td>187</td>
      <td>M7S</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>188</td>
      <td>M8S</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>189</td>
      <td>M9S</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>190</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Clarks Corners</td>
    </tr>
    <tr>
      <td>191</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Sullivan</td>
    </tr>
    <tr>
      <td>192</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Tam O'Shanter</td>
    </tr>
    <tr>
      <td>193</td>
      <td>M2T</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>194</td>
      <td>M3T</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>195</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Moore Park</td>
    </tr>
    <tr>
      <td>196</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Summerhill East</td>
    </tr>
    <tr>
      <td>197</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Chinatown</td>
    </tr>
    <tr>
      <td>198</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Grange Park</td>
    </tr>
    <tr>
      <td>199</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Kensington Market</td>
    </tr>
    <tr>
      <td>200</td>
      <td>M6T</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>201</td>
      <td>M7T</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>202</td>
      <td>M8T</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>203</td>
      <td>M9T</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>204</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North</td>
    </tr>
    <tr>
      <td>205</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>L'Amoreaux East</td>
    </tr>
    <tr>
      <td>206</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Milliken</td>
    </tr>
    <tr>
      <td>207</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Steeles East</td>
    </tr>
    <tr>
      <td>208</td>
      <td>M2V</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>209</td>
      <td>M3V</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>210</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Deer Park</td>
    </tr>
    <tr>
      <td>211</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Forest Hill SE</td>
    </tr>
    <tr>
      <td>212</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Rathnelly</td>
    </tr>
    <tr>
      <td>213</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>South Hill</td>
    </tr>
    <tr>
      <td>214</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Summerhill West</td>
    </tr>
    <tr>
      <td>215</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>CN Tower</td>
    </tr>
    <tr>
      <td>216</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Bathurst Quay</td>
    </tr>
    <tr>
      <td>217</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Island airport</td>
    </tr>
    <tr>
      <td>218</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront West</td>
    </tr>
    <tr>
      <td>219</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>King and Spadina</td>
    </tr>
    <tr>
      <td>220</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Railway Lands</td>
    </tr>
    <tr>
      <td>221</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>South Niagara</td>
    </tr>
    <tr>
      <td>222</td>
      <td>M6V</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>223</td>
      <td>M7V</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>224</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Humber Bay Shores</td>
    </tr>
    <tr>
      <td>225</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Mimico South</td>
    </tr>
    <tr>
      <td>226</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>New Toronto</td>
    </tr>
    <tr>
      <td>227</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens</td>
    </tr>
    <tr>
      <td>228</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Beaumond Heights</td>
    </tr>
    <tr>
      <td>229</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Humbergate</td>
    </tr>
    <tr>
      <td>230</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Jamestown</td>
    </tr>
    <tr>
      <td>231</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Mount Olive</td>
    </tr>
    <tr>
      <td>232</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Silverstone</td>
    </tr>
    <tr>
      <td>233</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>South Steeles</td>
    </tr>
    <tr>
      <td>234</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Thistletown</td>
    </tr>
    <tr>
      <td>235</td>
      <td>M1W</td>
      <td>Scarborough</td>
      <td>L'Amoreaux West</td>
    </tr>
    <tr>
      <td>236</td>
      <td>M2W</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>237</td>
      <td>M3W</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>238</td>
      <td>M4W</td>
      <td>Downtown Toronto</td>
      <td>Rosedale</td>
    </tr>
    <tr>
      <td>239</td>
      <td>M5W</td>
      <td>Downtown Toronto</td>
      <td>Stn A PO Boxes 25 The Esplanade</td>
    </tr>
    <tr>
      <td>240</td>
      <td>M6W</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>241</td>
      <td>M7W</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>242</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood</td>
    </tr>
    <tr>
      <td>243</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Long Branch</td>
    </tr>
    <tr>
      <td>244</td>
      <td>M9W</td>
      <td>Etobicoke</td>
      <td>Northwest</td>
    </tr>
    <tr>
      <td>245</td>
      <td>M1X</td>
      <td>Scarborough</td>
      <td>Upper Rouge</td>
    </tr>
    <tr>
      <td>246</td>
      <td>M2X</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>247</td>
      <td>M3X</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>248</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>Cabbagetown</td>
    </tr>
    <tr>
      <td>249</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
    </tr>
    <tr>
      <td>250</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>First Canadian Place</td>
    </tr>
    <tr>
      <td>251</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>Underground city</td>
    </tr>
    <tr>
      <td>252</td>
      <td>M6X</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>253</td>
      <td>M7X</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>254</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>The Kingsway</td>
    </tr>
    <tr>
      <td>255</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>Montgomery Road</td>
    </tr>
    <tr>
      <td>256</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>Old Mill North</td>
    </tr>
    <tr>
      <td>257</td>
      <td>M9X</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>258</td>
      <td>M1Y</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>259</td>
      <td>M2Y</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>260</td>
      <td>M3Y</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>261</td>
      <td>M4Y</td>
      <td>Downtown Toronto</td>
      <td>Church and Wellesley</td>
    </tr>
    <tr>
      <td>262</td>
      <td>M5Y</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>263</td>
      <td>M6Y</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>264</td>
      <td>M7Y</td>
      <td>East Toronto</td>
      <td>Business Reply Mail Processing Centre 969 Eastern</td>
    </tr>
    <tr>
      <td>265</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Humber Bay</td>
    </tr>
    <tr>
      <td>266</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>King's Mill Park</td>
    </tr>
    <tr>
      <td>267</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South East</td>
    </tr>
    <tr>
      <td>268</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Mimico NE</td>
    </tr>
    <tr>
      <td>269</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Old Mill South</td>
    </tr>
    <tr>
      <td>270</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>The Queensway East</td>
    </tr>
    <tr>
      <td>271</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Royal York South East</td>
    </tr>
    <tr>
      <td>272</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Sunnylea</td>
    </tr>
    <tr>
      <td>273</td>
      <td>M9Y</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>274</td>
      <td>M1Z</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>275</td>
      <td>M2Z</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>276</td>
      <td>M3Z</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>277</td>
      <td>M4Z</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>278</td>
      <td>M5Z</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>279</td>
      <td>M6Z</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>280</td>
      <td>M7Z</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>281</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South West</td>
    </tr>
    <tr>
      <td>282</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Mimico NW</td>
    </tr>
    <tr>
      <td>283</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>The Queensway West</td>
    </tr>
    <tr>
      <td>284</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Royal York South West</td>
    </tr>
    <tr>
      <td>285</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>South of Bloor</td>
    </tr>
    <tr>
      <td>286</td>
      <td>M9Z</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
  </tbody>
</table>
</div>




```python
my_dataframe.dtypes
```




    Postcode         object
    Borough          object
    Neighbourhood    object
    dtype: object




```python
h=my_dataframe.astype(str)
h.dtypes
```




    Postcode         object
    Borough          object
    Neighbourhood    object
    dtype: object



## Ignore cells with  "Borough" that is Not assigned.


```python
my_dataframe = my_dataframe[my_dataframe.Borough != 'Not assigned']
my_dataframe
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postcode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>2</td>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
    </tr>
    <tr>
      <td>3</td>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
    </tr>
    <tr>
      <td>4</td>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront</td>
    </tr>
    <tr>
      <td>5</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Heights</td>
    </tr>
    <tr>
      <td>6</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Manor</td>
    </tr>
    <tr>
      <td>7</td>
      <td>M7A</td>
      <td>Queen's Park</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>9</td>
      <td>M9A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park</td>
    </tr>
    <tr>
      <td>10</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge</td>
    </tr>
    <tr>
      <td>11</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Malvern</td>
    </tr>
    <tr>
      <td>13</td>
      <td>M3B</td>
      <td>North York</td>
      <td>Don Mills North</td>
    </tr>
    <tr>
      <td>14</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Woodbine Gardens</td>
    </tr>
    <tr>
      <td>15</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Parkview Hill</td>
    </tr>
    <tr>
      <td>16</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Ryerson</td>
    </tr>
    <tr>
      <td>17</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Garden District</td>
    </tr>
    <tr>
      <td>18</td>
      <td>M6B</td>
      <td>North York</td>
      <td>Glencairn</td>
    </tr>
    <tr>
      <td>21</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Cloverdale</td>
    </tr>
    <tr>
      <td>22</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Islington</td>
    </tr>
    <tr>
      <td>23</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Martin Grove</td>
    </tr>
    <tr>
      <td>24</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Princess Gardens</td>
    </tr>
    <tr>
      <td>25</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>West Deane Park</td>
    </tr>
    <tr>
      <td>26</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek</td>
    </tr>
    <tr>
      <td>27</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Rouge Hill</td>
    </tr>
    <tr>
      <td>28</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Port Union</td>
    </tr>
    <tr>
      <td>30</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Flemingdon Park</td>
    </tr>
    <tr>
      <td>31</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Don Mills South</td>
    </tr>
    <tr>
      <td>32</td>
      <td>M4C</td>
      <td>East York</td>
      <td>Woodbine Heights</td>
    </tr>
    <tr>
      <td>33</td>
      <td>M5C</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
    </tr>
    <tr>
      <td>34</td>
      <td>M6C</td>
      <td>York</td>
      <td>Humewood-Cedarvale</td>
    </tr>
    <tr>
      <td>37</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Bloordale Gardens</td>
    </tr>
    <tr>
      <td>38</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Eringate</td>
    </tr>
    <tr>
      <td>39</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Markland Wood</td>
    </tr>
    <tr>
      <td>40</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Old Burnhamthorpe</td>
    </tr>
    <tr>
      <td>41</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood</td>
    </tr>
    <tr>
      <td>42</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Morningside</td>
    </tr>
    <tr>
      <td>43</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>West Hill</td>
    </tr>
    <tr>
      <td>46</td>
      <td>M4E</td>
      <td>East Toronto</td>
      <td>The Beaches</td>
    </tr>
    <tr>
      <td>47</td>
      <td>M5E</td>
      <td>Downtown Toronto</td>
      <td>Berczy Park</td>
    </tr>
    <tr>
      <td>48</td>
      <td>M6E</td>
      <td>York</td>
      <td>Caledonia-Fairbanks</td>
    </tr>
    <tr>
      <td>52</td>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <td>55</td>
      <td>M4G</td>
      <td>East York</td>
      <td>Leaside</td>
    </tr>
    <tr>
      <td>56</td>
      <td>M5G</td>
      <td>Downtown Toronto</td>
      <td>Central Bay Street</td>
    </tr>
    <tr>
      <td>57</td>
      <td>M6G</td>
      <td>Downtown Toronto</td>
      <td>Christie</td>
    </tr>
    <tr>
      <td>61</td>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
    <tr>
      <td>62</td>
      <td>M2H</td>
      <td>North York</td>
      <td>Hillcrest Village</td>
    </tr>
    <tr>
      <td>63</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Bathurst Manor</td>
    </tr>
    <tr>
      <td>64</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Downsview North</td>
    </tr>
    <tr>
      <td>65</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Wilson Heights</td>
    </tr>
    <tr>
      <td>66</td>
      <td>M4H</td>
      <td>East York</td>
      <td>Thorncliffe Park</td>
    </tr>
    <tr>
      <td>67</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Adelaide</td>
    </tr>
    <tr>
      <td>68</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>King</td>
    </tr>
    <tr>
      <td>69</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Richmond</td>
    </tr>
    <tr>
      <td>70</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dovercourt Village</td>
    </tr>
    <tr>
      <td>71</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dufferin</td>
    </tr>
    <tr>
      <td>75</td>
      <td>M1J</td>
      <td>Scarborough</td>
      <td>Scarborough Village</td>
    </tr>
    <tr>
      <td>76</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Fairview</td>
    </tr>
    <tr>
      <td>77</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Henry Farm</td>
    </tr>
    <tr>
      <td>78</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Oriole</td>
    </tr>
    <tr>
      <td>79</td>
      <td>M3J</td>
      <td>North York</td>
      <td>Northwood Park</td>
    </tr>
    <tr>
      <td>80</td>
      <td>M3J</td>
      <td>North York</td>
      <td>York University</td>
    </tr>
    <tr>
      <td>81</td>
      <td>M4J</td>
      <td>East York</td>
      <td>East Toronto</td>
    </tr>
    <tr>
      <td>82</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront East</td>
    </tr>
    <tr>
      <td>83</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Toronto Islands</td>
    </tr>
    <tr>
      <td>84</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Union Station</td>
    </tr>
    <tr>
      <td>85</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Little Portugal</td>
    </tr>
    <tr>
      <td>86</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Trinity</td>
    </tr>
    <tr>
      <td>90</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>East Birchmount Park</td>
    </tr>
    <tr>
      <td>91</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>Ionview</td>
    </tr>
    <tr>
      <td>92</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>Kennedy Park</td>
    </tr>
    <tr>
      <td>93</td>
      <td>M2K</td>
      <td>North York</td>
      <td>Bayview Village</td>
    </tr>
    <tr>
      <td>94</td>
      <td>M3K</td>
      <td>North York</td>
      <td>CFB Toronto</td>
    </tr>
    <tr>
      <td>95</td>
      <td>M3K</td>
      <td>North York</td>
      <td>Downsview East</td>
    </tr>
    <tr>
      <td>96</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>The Danforth West</td>
    </tr>
    <tr>
      <td>97</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>Riverdale</td>
    </tr>
    <tr>
      <td>98</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Design Exchange</td>
    </tr>
    <tr>
      <td>99</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Toronto Dominion Centre</td>
    </tr>
    <tr>
      <td>100</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Brockton</td>
    </tr>
    <tr>
      <td>101</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Exhibition Place</td>
    </tr>
    <tr>
      <td>102</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Parkdale Village</td>
    </tr>
    <tr>
      <td>106</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Clairlea</td>
    </tr>
    <tr>
      <td>107</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Golden Mile</td>
    </tr>
    <tr>
      <td>108</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Oakridge</td>
    </tr>
    <tr>
      <td>109</td>
      <td>M2L</td>
      <td>North York</td>
      <td>Silver Hills</td>
    </tr>
    <tr>
      <td>110</td>
      <td>M2L</td>
      <td>North York</td>
      <td>York Mills</td>
    </tr>
    <tr>
      <td>111</td>
      <td>M3L</td>
      <td>North York</td>
      <td>Downsview West</td>
    </tr>
    <tr>
      <td>112</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>The Beaches West</td>
    </tr>
    <tr>
      <td>113</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>India Bazaar</td>
    </tr>
    <tr>
      <td>114</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Commerce Court</td>
    </tr>
    <tr>
      <td>115</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Victoria Hotel</td>
    </tr>
    <tr>
      <td>116</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Downsview</td>
    </tr>
    <tr>
      <td>117</td>
      <td>M6L</td>
      <td>North York</td>
      <td>North Park</td>
    </tr>
    <tr>
      <td>118</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Upwood Park</td>
    </tr>
    <tr>
      <td>121</td>
      <td>M9L</td>
      <td>North York</td>
      <td>Humber Summit</td>
    </tr>
    <tr>
      <td>122</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffcrest</td>
    </tr>
    <tr>
      <td>123</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffside</td>
    </tr>
    <tr>
      <td>124</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Scarborough Village West</td>
    </tr>
    <tr>
      <td>125</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Newtonbrook</td>
    </tr>
    <tr>
      <td>126</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Willowdale</td>
    </tr>
    <tr>
      <td>127</td>
      <td>M3M</td>
      <td>North York</td>
      <td>Downsview Central</td>
    </tr>
    <tr>
      <td>128</td>
      <td>M4M</td>
      <td>East Toronto</td>
      <td>Studio District</td>
    </tr>
    <tr>
      <td>129</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Bedford Park</td>
    </tr>
    <tr>
      <td>130</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Lawrence Manor East</td>
    </tr>
    <tr>
      <td>131</td>
      <td>M6M</td>
      <td>York</td>
      <td>Del Ray</td>
    </tr>
    <tr>
      <td>132</td>
      <td>M6M</td>
      <td>York</td>
      <td>Keelesdale</td>
    </tr>
    <tr>
      <td>133</td>
      <td>M6M</td>
      <td>York</td>
      <td>Mount Dennis</td>
    </tr>
    <tr>
      <td>134</td>
      <td>M6M</td>
      <td>York</td>
      <td>Silverthorn</td>
    </tr>
    <tr>
      <td>137</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Emery</td>
    </tr>
    <tr>
      <td>138</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Humberlea</td>
    </tr>
    <tr>
      <td>139</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Birch Cliff</td>
    </tr>
    <tr>
      <td>140</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Cliffside West</td>
    </tr>
    <tr>
      <td>141</td>
      <td>M2N</td>
      <td>North York</td>
      <td>Willowdale South</td>
    </tr>
    <tr>
      <td>142</td>
      <td>M3N</td>
      <td>North York</td>
      <td>Downsview Northwest</td>
    </tr>
    <tr>
      <td>143</td>
      <td>M4N</td>
      <td>Central Toronto</td>
      <td>Lawrence Park</td>
    </tr>
    <tr>
      <td>144</td>
      <td>M5N</td>
      <td>Central Toronto</td>
      <td>Roselawn</td>
    </tr>
    <tr>
      <td>145</td>
      <td>M6N</td>
      <td>York</td>
      <td>The Junction North</td>
    </tr>
    <tr>
      <td>146</td>
      <td>M6N</td>
      <td>York</td>
      <td>Runnymede</td>
    </tr>
    <tr>
      <td>149</td>
      <td>M9N</td>
      <td>York</td>
      <td>Weston</td>
    </tr>
    <tr>
      <td>150</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Dorset Park</td>
    </tr>
    <tr>
      <td>151</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Scarborough Town Centre</td>
    </tr>
    <tr>
      <td>152</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Wexford Heights</td>
    </tr>
    <tr>
      <td>153</td>
      <td>M2P</td>
      <td>North York</td>
      <td>York Mills West</td>
    </tr>
    <tr>
      <td>155</td>
      <td>M4P</td>
      <td>Central Toronto</td>
      <td>Davisville North</td>
    </tr>
    <tr>
      <td>156</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill North</td>
    </tr>
    <tr>
      <td>157</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill West</td>
    </tr>
    <tr>
      <td>158</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>High Park</td>
    </tr>
    <tr>
      <td>159</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>The Junction South</td>
    </tr>
    <tr>
      <td>162</td>
      <td>M9P</td>
      <td>Etobicoke</td>
      <td>Westmount</td>
    </tr>
    <tr>
      <td>163</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Maryvale</td>
    </tr>
    <tr>
      <td>164</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Wexford</td>
    </tr>
    <tr>
      <td>165</td>
      <td>M2R</td>
      <td>North York</td>
      <td>Willowdale West</td>
    </tr>
    <tr>
      <td>167</td>
      <td>M4R</td>
      <td>Central Toronto</td>
      <td>North Toronto West</td>
    </tr>
    <tr>
      <td>168</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>The Annex</td>
    </tr>
    <tr>
      <td>169</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>North Midtown</td>
    </tr>
    <tr>
      <td>170</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>Yorkville</td>
    </tr>
    <tr>
      <td>171</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Parkdale</td>
    </tr>
    <tr>
      <td>172</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Roncesvalles</td>
    </tr>
    <tr>
      <td>173</td>
      <td>M7R</td>
      <td>Mississauga</td>
      <td>Canada Post Gateway Processing Centre</td>
    </tr>
    <tr>
      <td>175</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Kingsview Village</td>
    </tr>
    <tr>
      <td>176</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Martin Grove Gardens</td>
    </tr>
    <tr>
      <td>177</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Richview Gardens</td>
    </tr>
    <tr>
      <td>178</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>St. Phillips</td>
    </tr>
    <tr>
      <td>179</td>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
    </tr>
    <tr>
      <td>182</td>
      <td>M4S</td>
      <td>Central Toronto</td>
      <td>Davisville</td>
    </tr>
    <tr>
      <td>183</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>Harbord</td>
    </tr>
    <tr>
      <td>184</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>University of Toronto</td>
    </tr>
    <tr>
      <td>185</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Runnymede</td>
    </tr>
    <tr>
      <td>186</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Swansea</td>
    </tr>
    <tr>
      <td>190</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Clarks Corners</td>
    </tr>
    <tr>
      <td>191</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Sullivan</td>
    </tr>
    <tr>
      <td>192</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Tam O'Shanter</td>
    </tr>
    <tr>
      <td>195</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Moore Park</td>
    </tr>
    <tr>
      <td>196</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Summerhill East</td>
    </tr>
    <tr>
      <td>197</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Chinatown</td>
    </tr>
    <tr>
      <td>198</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Grange Park</td>
    </tr>
    <tr>
      <td>199</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Kensington Market</td>
    </tr>
    <tr>
      <td>204</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North</td>
    </tr>
    <tr>
      <td>205</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>L'Amoreaux East</td>
    </tr>
    <tr>
      <td>206</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Milliken</td>
    </tr>
    <tr>
      <td>207</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Steeles East</td>
    </tr>
    <tr>
      <td>210</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Deer Park</td>
    </tr>
    <tr>
      <td>211</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Forest Hill SE</td>
    </tr>
    <tr>
      <td>212</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Rathnelly</td>
    </tr>
    <tr>
      <td>213</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>South Hill</td>
    </tr>
    <tr>
      <td>214</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Summerhill West</td>
    </tr>
    <tr>
      <td>215</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>CN Tower</td>
    </tr>
    <tr>
      <td>216</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Bathurst Quay</td>
    </tr>
    <tr>
      <td>217</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Island airport</td>
    </tr>
    <tr>
      <td>218</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront West</td>
    </tr>
    <tr>
      <td>219</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>King and Spadina</td>
    </tr>
    <tr>
      <td>220</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Railway Lands</td>
    </tr>
    <tr>
      <td>221</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>South Niagara</td>
    </tr>
    <tr>
      <td>224</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Humber Bay Shores</td>
    </tr>
    <tr>
      <td>225</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Mimico South</td>
    </tr>
    <tr>
      <td>226</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>New Toronto</td>
    </tr>
    <tr>
      <td>227</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens</td>
    </tr>
    <tr>
      <td>228</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Beaumond Heights</td>
    </tr>
    <tr>
      <td>229</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Humbergate</td>
    </tr>
    <tr>
      <td>230</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Jamestown</td>
    </tr>
    <tr>
      <td>231</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Mount Olive</td>
    </tr>
    <tr>
      <td>232</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Silverstone</td>
    </tr>
    <tr>
      <td>233</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>South Steeles</td>
    </tr>
    <tr>
      <td>234</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Thistletown</td>
    </tr>
    <tr>
      <td>235</td>
      <td>M1W</td>
      <td>Scarborough</td>
      <td>L'Amoreaux West</td>
    </tr>
    <tr>
      <td>238</td>
      <td>M4W</td>
      <td>Downtown Toronto</td>
      <td>Rosedale</td>
    </tr>
    <tr>
      <td>239</td>
      <td>M5W</td>
      <td>Downtown Toronto</td>
      <td>Stn A PO Boxes 25 The Esplanade</td>
    </tr>
    <tr>
      <td>242</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood</td>
    </tr>
    <tr>
      <td>243</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Long Branch</td>
    </tr>
    <tr>
      <td>244</td>
      <td>M9W</td>
      <td>Etobicoke</td>
      <td>Northwest</td>
    </tr>
    <tr>
      <td>245</td>
      <td>M1X</td>
      <td>Scarborough</td>
      <td>Upper Rouge</td>
    </tr>
    <tr>
      <td>248</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>Cabbagetown</td>
    </tr>
    <tr>
      <td>249</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
    </tr>
    <tr>
      <td>250</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>First Canadian Place</td>
    </tr>
    <tr>
      <td>251</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>Underground city</td>
    </tr>
    <tr>
      <td>254</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>The Kingsway</td>
    </tr>
    <tr>
      <td>255</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>Montgomery Road</td>
    </tr>
    <tr>
      <td>256</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>Old Mill North</td>
    </tr>
    <tr>
      <td>261</td>
      <td>M4Y</td>
      <td>Downtown Toronto</td>
      <td>Church and Wellesley</td>
    </tr>
    <tr>
      <td>264</td>
      <td>M7Y</td>
      <td>East Toronto</td>
      <td>Business Reply Mail Processing Centre 969 Eastern</td>
    </tr>
    <tr>
      <td>265</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Humber Bay</td>
    </tr>
    <tr>
      <td>266</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>King's Mill Park</td>
    </tr>
    <tr>
      <td>267</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South East</td>
    </tr>
    <tr>
      <td>268</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Mimico NE</td>
    </tr>
    <tr>
      <td>269</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Old Mill South</td>
    </tr>
    <tr>
      <td>270</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>The Queensway East</td>
    </tr>
    <tr>
      <td>271</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Royal York South East</td>
    </tr>
    <tr>
      <td>272</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Sunnylea</td>
    </tr>
    <tr>
      <td>281</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South West</td>
    </tr>
    <tr>
      <td>282</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Mimico NW</td>
    </tr>
    <tr>
      <td>283</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>The Queensway West</td>
    </tr>
    <tr>
      <td>284</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Royal York South West</td>
    </tr>
    <tr>
      <td>285</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>South of Bloor</td>
    </tr>
  </tbody>
</table>
</div>



## Group by "PostCode"


```python
pd.set_option('display.max_rows', None)
my_dataframe.groupby(['Postcode'])
my_dataframe
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postcode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>2</td>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
    </tr>
    <tr>
      <td>3</td>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
    </tr>
    <tr>
      <td>4</td>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront</td>
    </tr>
    <tr>
      <td>5</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Heights</td>
    </tr>
    <tr>
      <td>6</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Manor</td>
    </tr>
    <tr>
      <td>7</td>
      <td>M7A</td>
      <td>Queen's Park</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>9</td>
      <td>M9A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park</td>
    </tr>
    <tr>
      <td>10</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge</td>
    </tr>
    <tr>
      <td>11</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Malvern</td>
    </tr>
    <tr>
      <td>13</td>
      <td>M3B</td>
      <td>North York</td>
      <td>Don Mills North</td>
    </tr>
    <tr>
      <td>14</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Woodbine Gardens</td>
    </tr>
    <tr>
      <td>15</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Parkview Hill</td>
    </tr>
    <tr>
      <td>16</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Ryerson</td>
    </tr>
    <tr>
      <td>17</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Garden District</td>
    </tr>
    <tr>
      <td>18</td>
      <td>M6B</td>
      <td>North York</td>
      <td>Glencairn</td>
    </tr>
    <tr>
      <td>21</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Cloverdale</td>
    </tr>
    <tr>
      <td>22</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Islington</td>
    </tr>
    <tr>
      <td>23</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Martin Grove</td>
    </tr>
    <tr>
      <td>24</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Princess Gardens</td>
    </tr>
    <tr>
      <td>25</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>West Deane Park</td>
    </tr>
    <tr>
      <td>26</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek</td>
    </tr>
    <tr>
      <td>27</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Rouge Hill</td>
    </tr>
    <tr>
      <td>28</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Port Union</td>
    </tr>
    <tr>
      <td>30</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Flemingdon Park</td>
    </tr>
    <tr>
      <td>31</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Don Mills South</td>
    </tr>
    <tr>
      <td>32</td>
      <td>M4C</td>
      <td>East York</td>
      <td>Woodbine Heights</td>
    </tr>
    <tr>
      <td>33</td>
      <td>M5C</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
    </tr>
    <tr>
      <td>34</td>
      <td>M6C</td>
      <td>York</td>
      <td>Humewood-Cedarvale</td>
    </tr>
    <tr>
      <td>37</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Bloordale Gardens</td>
    </tr>
    <tr>
      <td>38</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Eringate</td>
    </tr>
    <tr>
      <td>39</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Markland Wood</td>
    </tr>
    <tr>
      <td>40</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Old Burnhamthorpe</td>
    </tr>
    <tr>
      <td>41</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood</td>
    </tr>
    <tr>
      <td>42</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Morningside</td>
    </tr>
    <tr>
      <td>43</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>West Hill</td>
    </tr>
    <tr>
      <td>46</td>
      <td>M4E</td>
      <td>East Toronto</td>
      <td>The Beaches</td>
    </tr>
    <tr>
      <td>47</td>
      <td>M5E</td>
      <td>Downtown Toronto</td>
      <td>Berczy Park</td>
    </tr>
    <tr>
      <td>48</td>
      <td>M6E</td>
      <td>York</td>
      <td>Caledonia-Fairbanks</td>
    </tr>
    <tr>
      <td>52</td>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <td>55</td>
      <td>M4G</td>
      <td>East York</td>
      <td>Leaside</td>
    </tr>
    <tr>
      <td>56</td>
      <td>M5G</td>
      <td>Downtown Toronto</td>
      <td>Central Bay Street</td>
    </tr>
    <tr>
      <td>57</td>
      <td>M6G</td>
      <td>Downtown Toronto</td>
      <td>Christie</td>
    </tr>
    <tr>
      <td>61</td>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
    <tr>
      <td>62</td>
      <td>M2H</td>
      <td>North York</td>
      <td>Hillcrest Village</td>
    </tr>
    <tr>
      <td>63</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Bathurst Manor</td>
    </tr>
    <tr>
      <td>64</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Downsview North</td>
    </tr>
    <tr>
      <td>65</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Wilson Heights</td>
    </tr>
    <tr>
      <td>66</td>
      <td>M4H</td>
      <td>East York</td>
      <td>Thorncliffe Park</td>
    </tr>
    <tr>
      <td>67</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Adelaide</td>
    </tr>
    <tr>
      <td>68</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>King</td>
    </tr>
    <tr>
      <td>69</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Richmond</td>
    </tr>
    <tr>
      <td>70</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dovercourt Village</td>
    </tr>
    <tr>
      <td>71</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dufferin</td>
    </tr>
    <tr>
      <td>75</td>
      <td>M1J</td>
      <td>Scarborough</td>
      <td>Scarborough Village</td>
    </tr>
    <tr>
      <td>76</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Fairview</td>
    </tr>
    <tr>
      <td>77</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Henry Farm</td>
    </tr>
    <tr>
      <td>78</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Oriole</td>
    </tr>
    <tr>
      <td>79</td>
      <td>M3J</td>
      <td>North York</td>
      <td>Northwood Park</td>
    </tr>
    <tr>
      <td>80</td>
      <td>M3J</td>
      <td>North York</td>
      <td>York University</td>
    </tr>
    <tr>
      <td>81</td>
      <td>M4J</td>
      <td>East York</td>
      <td>East Toronto</td>
    </tr>
    <tr>
      <td>82</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront East</td>
    </tr>
    <tr>
      <td>83</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Toronto Islands</td>
    </tr>
    <tr>
      <td>84</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Union Station</td>
    </tr>
    <tr>
      <td>85</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Little Portugal</td>
    </tr>
    <tr>
      <td>86</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Trinity</td>
    </tr>
    <tr>
      <td>90</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>East Birchmount Park</td>
    </tr>
    <tr>
      <td>91</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>Ionview</td>
    </tr>
    <tr>
      <td>92</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>Kennedy Park</td>
    </tr>
    <tr>
      <td>93</td>
      <td>M2K</td>
      <td>North York</td>
      <td>Bayview Village</td>
    </tr>
    <tr>
      <td>94</td>
      <td>M3K</td>
      <td>North York</td>
      <td>CFB Toronto</td>
    </tr>
    <tr>
      <td>95</td>
      <td>M3K</td>
      <td>North York</td>
      <td>Downsview East</td>
    </tr>
    <tr>
      <td>96</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>The Danforth West</td>
    </tr>
    <tr>
      <td>97</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>Riverdale</td>
    </tr>
    <tr>
      <td>98</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Design Exchange</td>
    </tr>
    <tr>
      <td>99</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Toronto Dominion Centre</td>
    </tr>
    <tr>
      <td>100</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Brockton</td>
    </tr>
    <tr>
      <td>101</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Exhibition Place</td>
    </tr>
    <tr>
      <td>102</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Parkdale Village</td>
    </tr>
    <tr>
      <td>106</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Clairlea</td>
    </tr>
    <tr>
      <td>107</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Golden Mile</td>
    </tr>
    <tr>
      <td>108</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Oakridge</td>
    </tr>
    <tr>
      <td>109</td>
      <td>M2L</td>
      <td>North York</td>
      <td>Silver Hills</td>
    </tr>
    <tr>
      <td>110</td>
      <td>M2L</td>
      <td>North York</td>
      <td>York Mills</td>
    </tr>
    <tr>
      <td>111</td>
      <td>M3L</td>
      <td>North York</td>
      <td>Downsview West</td>
    </tr>
    <tr>
      <td>112</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>The Beaches West</td>
    </tr>
    <tr>
      <td>113</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>India Bazaar</td>
    </tr>
    <tr>
      <td>114</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Commerce Court</td>
    </tr>
    <tr>
      <td>115</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Victoria Hotel</td>
    </tr>
    <tr>
      <td>116</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Downsview</td>
    </tr>
    <tr>
      <td>117</td>
      <td>M6L</td>
      <td>North York</td>
      <td>North Park</td>
    </tr>
    <tr>
      <td>118</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Upwood Park</td>
    </tr>
    <tr>
      <td>121</td>
      <td>M9L</td>
      <td>North York</td>
      <td>Humber Summit</td>
    </tr>
    <tr>
      <td>122</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffcrest</td>
    </tr>
    <tr>
      <td>123</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffside</td>
    </tr>
    <tr>
      <td>124</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Scarborough Village West</td>
    </tr>
    <tr>
      <td>125</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Newtonbrook</td>
    </tr>
    <tr>
      <td>126</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Willowdale</td>
    </tr>
    <tr>
      <td>127</td>
      <td>M3M</td>
      <td>North York</td>
      <td>Downsview Central</td>
    </tr>
    <tr>
      <td>128</td>
      <td>M4M</td>
      <td>East Toronto</td>
      <td>Studio District</td>
    </tr>
    <tr>
      <td>129</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Bedford Park</td>
    </tr>
    <tr>
      <td>130</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Lawrence Manor East</td>
    </tr>
    <tr>
      <td>131</td>
      <td>M6M</td>
      <td>York</td>
      <td>Del Ray</td>
    </tr>
    <tr>
      <td>132</td>
      <td>M6M</td>
      <td>York</td>
      <td>Keelesdale</td>
    </tr>
    <tr>
      <td>133</td>
      <td>M6M</td>
      <td>York</td>
      <td>Mount Dennis</td>
    </tr>
    <tr>
      <td>134</td>
      <td>M6M</td>
      <td>York</td>
      <td>Silverthorn</td>
    </tr>
    <tr>
      <td>137</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Emery</td>
    </tr>
    <tr>
      <td>138</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Humberlea</td>
    </tr>
    <tr>
      <td>139</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Birch Cliff</td>
    </tr>
    <tr>
      <td>140</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Cliffside West</td>
    </tr>
    <tr>
      <td>141</td>
      <td>M2N</td>
      <td>North York</td>
      <td>Willowdale South</td>
    </tr>
    <tr>
      <td>142</td>
      <td>M3N</td>
      <td>North York</td>
      <td>Downsview Northwest</td>
    </tr>
    <tr>
      <td>143</td>
      <td>M4N</td>
      <td>Central Toronto</td>
      <td>Lawrence Park</td>
    </tr>
    <tr>
      <td>144</td>
      <td>M5N</td>
      <td>Central Toronto</td>
      <td>Roselawn</td>
    </tr>
    <tr>
      <td>145</td>
      <td>M6N</td>
      <td>York</td>
      <td>The Junction North</td>
    </tr>
    <tr>
      <td>146</td>
      <td>M6N</td>
      <td>York</td>
      <td>Runnymede</td>
    </tr>
    <tr>
      <td>149</td>
      <td>M9N</td>
      <td>York</td>
      <td>Weston</td>
    </tr>
    <tr>
      <td>150</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Dorset Park</td>
    </tr>
    <tr>
      <td>151</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Scarborough Town Centre</td>
    </tr>
    <tr>
      <td>152</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Wexford Heights</td>
    </tr>
    <tr>
      <td>153</td>
      <td>M2P</td>
      <td>North York</td>
      <td>York Mills West</td>
    </tr>
    <tr>
      <td>155</td>
      <td>M4P</td>
      <td>Central Toronto</td>
      <td>Davisville North</td>
    </tr>
    <tr>
      <td>156</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill North</td>
    </tr>
    <tr>
      <td>157</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill West</td>
    </tr>
    <tr>
      <td>158</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>High Park</td>
    </tr>
    <tr>
      <td>159</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>The Junction South</td>
    </tr>
    <tr>
      <td>162</td>
      <td>M9P</td>
      <td>Etobicoke</td>
      <td>Westmount</td>
    </tr>
    <tr>
      <td>163</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Maryvale</td>
    </tr>
    <tr>
      <td>164</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Wexford</td>
    </tr>
    <tr>
      <td>165</td>
      <td>M2R</td>
      <td>North York</td>
      <td>Willowdale West</td>
    </tr>
    <tr>
      <td>167</td>
      <td>M4R</td>
      <td>Central Toronto</td>
      <td>North Toronto West</td>
    </tr>
    <tr>
      <td>168</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>The Annex</td>
    </tr>
    <tr>
      <td>169</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>North Midtown</td>
    </tr>
    <tr>
      <td>170</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>Yorkville</td>
    </tr>
    <tr>
      <td>171</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Parkdale</td>
    </tr>
    <tr>
      <td>172</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Roncesvalles</td>
    </tr>
    <tr>
      <td>173</td>
      <td>M7R</td>
      <td>Mississauga</td>
      <td>Canada Post Gateway Processing Centre</td>
    </tr>
    <tr>
      <td>175</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Kingsview Village</td>
    </tr>
    <tr>
      <td>176</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Martin Grove Gardens</td>
    </tr>
    <tr>
      <td>177</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Richview Gardens</td>
    </tr>
    <tr>
      <td>178</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>St. Phillips</td>
    </tr>
    <tr>
      <td>179</td>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
    </tr>
    <tr>
      <td>182</td>
      <td>M4S</td>
      <td>Central Toronto</td>
      <td>Davisville</td>
    </tr>
    <tr>
      <td>183</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>Harbord</td>
    </tr>
    <tr>
      <td>184</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>University of Toronto</td>
    </tr>
    <tr>
      <td>185</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Runnymede</td>
    </tr>
    <tr>
      <td>186</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Swansea</td>
    </tr>
    <tr>
      <td>190</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Clarks Corners</td>
    </tr>
    <tr>
      <td>191</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Sullivan</td>
    </tr>
    <tr>
      <td>192</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Tam O'Shanter</td>
    </tr>
    <tr>
      <td>195</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Moore Park</td>
    </tr>
    <tr>
      <td>196</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Summerhill East</td>
    </tr>
    <tr>
      <td>197</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Chinatown</td>
    </tr>
    <tr>
      <td>198</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Grange Park</td>
    </tr>
    <tr>
      <td>199</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Kensington Market</td>
    </tr>
    <tr>
      <td>204</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North</td>
    </tr>
    <tr>
      <td>205</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>L'Amoreaux East</td>
    </tr>
    <tr>
      <td>206</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Milliken</td>
    </tr>
    <tr>
      <td>207</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Steeles East</td>
    </tr>
    <tr>
      <td>210</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Deer Park</td>
    </tr>
    <tr>
      <td>211</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Forest Hill SE</td>
    </tr>
    <tr>
      <td>212</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Rathnelly</td>
    </tr>
    <tr>
      <td>213</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>South Hill</td>
    </tr>
    <tr>
      <td>214</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Summerhill West</td>
    </tr>
    <tr>
      <td>215</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>CN Tower</td>
    </tr>
    <tr>
      <td>216</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Bathurst Quay</td>
    </tr>
    <tr>
      <td>217</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Island airport</td>
    </tr>
    <tr>
      <td>218</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront West</td>
    </tr>
    <tr>
      <td>219</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>King and Spadina</td>
    </tr>
    <tr>
      <td>220</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>Railway Lands</td>
    </tr>
    <tr>
      <td>221</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>South Niagara</td>
    </tr>
    <tr>
      <td>224</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Humber Bay Shores</td>
    </tr>
    <tr>
      <td>225</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Mimico South</td>
    </tr>
    <tr>
      <td>226</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>New Toronto</td>
    </tr>
    <tr>
      <td>227</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens</td>
    </tr>
    <tr>
      <td>228</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Beaumond Heights</td>
    </tr>
    <tr>
      <td>229</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Humbergate</td>
    </tr>
    <tr>
      <td>230</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Jamestown</td>
    </tr>
    <tr>
      <td>231</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Mount Olive</td>
    </tr>
    <tr>
      <td>232</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Silverstone</td>
    </tr>
    <tr>
      <td>233</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>South Steeles</td>
    </tr>
    <tr>
      <td>234</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Thistletown</td>
    </tr>
    <tr>
      <td>235</td>
      <td>M1W</td>
      <td>Scarborough</td>
      <td>L'Amoreaux West</td>
    </tr>
    <tr>
      <td>238</td>
      <td>M4W</td>
      <td>Downtown Toronto</td>
      <td>Rosedale</td>
    </tr>
    <tr>
      <td>239</td>
      <td>M5W</td>
      <td>Downtown Toronto</td>
      <td>Stn A PO Boxes 25 The Esplanade</td>
    </tr>
    <tr>
      <td>242</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood</td>
    </tr>
    <tr>
      <td>243</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Long Branch</td>
    </tr>
    <tr>
      <td>244</td>
      <td>M9W</td>
      <td>Etobicoke</td>
      <td>Northwest</td>
    </tr>
    <tr>
      <td>245</td>
      <td>M1X</td>
      <td>Scarborough</td>
      <td>Upper Rouge</td>
    </tr>
    <tr>
      <td>248</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>Cabbagetown</td>
    </tr>
    <tr>
      <td>249</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
    </tr>
    <tr>
      <td>250</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>First Canadian Place</td>
    </tr>
    <tr>
      <td>251</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>Underground city</td>
    </tr>
    <tr>
      <td>254</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>The Kingsway</td>
    </tr>
    <tr>
      <td>255</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>Montgomery Road</td>
    </tr>
    <tr>
      <td>256</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>Old Mill North</td>
    </tr>
    <tr>
      <td>261</td>
      <td>M4Y</td>
      <td>Downtown Toronto</td>
      <td>Church and Wellesley</td>
    </tr>
    <tr>
      <td>264</td>
      <td>M7Y</td>
      <td>East Toronto</td>
      <td>Business Reply Mail Processing Centre 969 Eastern</td>
    </tr>
    <tr>
      <td>265</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Humber Bay</td>
    </tr>
    <tr>
      <td>266</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>King's Mill Park</td>
    </tr>
    <tr>
      <td>267</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South East</td>
    </tr>
    <tr>
      <td>268</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Mimico NE</td>
    </tr>
    <tr>
      <td>269</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Old Mill South</td>
    </tr>
    <tr>
      <td>270</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>The Queensway East</td>
    </tr>
    <tr>
      <td>271</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Royal York South East</td>
    </tr>
    <tr>
      <td>272</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Sunnylea</td>
    </tr>
    <tr>
      <td>281</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South West</td>
    </tr>
    <tr>
      <td>282</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Mimico NW</td>
    </tr>
    <tr>
      <td>283</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>The Queensway West</td>
    </tr>
    <tr>
      <td>284</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Royal York South West</td>
    </tr>
    <tr>
      <td>285</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>South of Bloor</td>
    </tr>
  </tbody>
</table>
</div>




```python
my_dataframe.at[3,'Postcode']
```




    'M4A'



## Same "Neighborhoods" separated with a comma 


```python
#Y=my_dataframe.groupby(['Postcode','Borough',],as_index=True).Neighbourhood.agg([ ('Neighbourhood10', ', '.join)])

Y=my_dataframe.groupby(['Postcode','Borough',],as_index=True).Neighbourhood.agg([ ('Neighbourhood', ', '.join)])
Y

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>Neighbourhood</th>
    </tr>
    <tr>
      <th>Postcode</th>
      <th>Borough</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge, Malvern</td>
    </tr>
    <tr>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek, Rouge Hill, Port Union</td>
    </tr>
    <tr>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood, Morningside, West Hill</td>
    </tr>
    <tr>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
    <tr>
      <td>M1J</td>
      <td>Scarborough</td>
      <td>Scarborough Village</td>
    </tr>
    <tr>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>East Birchmount Park, Ionview, Kennedy Park</td>
    </tr>
    <tr>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Clairlea, Golden Mile, Oakridge</td>
    </tr>
    <tr>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffcrest, Cliffside, Scarborough Village West</td>
    </tr>
    <tr>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Birch Cliff, Cliffside West</td>
    </tr>
    <tr>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Dorset Park, Scarborough Town Centre, Wexford ...</td>
    </tr>
    <tr>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Maryvale, Wexford</td>
    </tr>
    <tr>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
    </tr>
    <tr>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Clarks Corners, Sullivan, Tam O'Shanter</td>
    </tr>
    <tr>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North, L'Amoreaux East, Milliken, St...</td>
    </tr>
    <tr>
      <td>M1W</td>
      <td>Scarborough</td>
      <td>L'Amoreaux West</td>
    </tr>
    <tr>
      <td>M1X</td>
      <td>Scarborough</td>
      <td>Upper Rouge</td>
    </tr>
    <tr>
      <td>M2H</td>
      <td>North York</td>
      <td>Hillcrest Village</td>
    </tr>
    <tr>
      <td>M2J</td>
      <td>North York</td>
      <td>Fairview, Henry Farm, Oriole</td>
    </tr>
    <tr>
      <td>M2K</td>
      <td>North York</td>
      <td>Bayview Village</td>
    </tr>
    <tr>
      <td>M2L</td>
      <td>North York</td>
      <td>Silver Hills, York Mills</td>
    </tr>
    <tr>
      <td>M2M</td>
      <td>North York</td>
      <td>Newtonbrook, Willowdale</td>
    </tr>
    <tr>
      <td>M2N</td>
      <td>North York</td>
      <td>Willowdale South</td>
    </tr>
    <tr>
      <td>M2P</td>
      <td>North York</td>
      <td>York Mills West</td>
    </tr>
    <tr>
      <td>M2R</td>
      <td>North York</td>
      <td>Willowdale West</td>
    </tr>
    <tr>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
    </tr>
    <tr>
      <td>M3B</td>
      <td>North York</td>
      <td>Don Mills North</td>
    </tr>
    <tr>
      <td>M3C</td>
      <td>North York</td>
      <td>Flemingdon Park, Don Mills South</td>
    </tr>
    <tr>
      <td>M3H</td>
      <td>North York</td>
      <td>Bathurst Manor, Downsview North, Wilson Heights</td>
    </tr>
    <tr>
      <td>M3J</td>
      <td>North York</td>
      <td>Northwood Park, York University</td>
    </tr>
    <tr>
      <td>M3K</td>
      <td>North York</td>
      <td>CFB Toronto, Downsview East</td>
    </tr>
    <tr>
      <td>M3L</td>
      <td>North York</td>
      <td>Downsview West</td>
    </tr>
    <tr>
      <td>M3M</td>
      <td>North York</td>
      <td>Downsview Central</td>
    </tr>
    <tr>
      <td>M3N</td>
      <td>North York</td>
      <td>Downsview Northwest</td>
    </tr>
    <tr>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
    </tr>
    <tr>
      <td>M4B</td>
      <td>East York</td>
      <td>Woodbine Gardens, Parkview Hill</td>
    </tr>
    <tr>
      <td>M4C</td>
      <td>East York</td>
      <td>Woodbine Heights</td>
    </tr>
    <tr>
      <td>M4E</td>
      <td>East Toronto</td>
      <td>The Beaches</td>
    </tr>
    <tr>
      <td>M4G</td>
      <td>East York</td>
      <td>Leaside</td>
    </tr>
    <tr>
      <td>M4H</td>
      <td>East York</td>
      <td>Thorncliffe Park</td>
    </tr>
    <tr>
      <td>M4J</td>
      <td>East York</td>
      <td>East Toronto</td>
    </tr>
    <tr>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>The Danforth West, Riverdale</td>
    </tr>
    <tr>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>The Beaches West, India Bazaar</td>
    </tr>
    <tr>
      <td>M4M</td>
      <td>East Toronto</td>
      <td>Studio District</td>
    </tr>
    <tr>
      <td>M4N</td>
      <td>Central Toronto</td>
      <td>Lawrence Park</td>
    </tr>
    <tr>
      <td>M4P</td>
      <td>Central Toronto</td>
      <td>Davisville North</td>
    </tr>
    <tr>
      <td>M4R</td>
      <td>Central Toronto</td>
      <td>North Toronto West</td>
    </tr>
    <tr>
      <td>M4S</td>
      <td>Central Toronto</td>
      <td>Davisville</td>
    </tr>
    <tr>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Moore Park, Summerhill East</td>
    </tr>
    <tr>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Deer Park, Forest Hill SE, Rathnelly, South Hi...</td>
    </tr>
    <tr>
      <td>M4W</td>
      <td>Downtown Toronto</td>
      <td>Rosedale</td>
    </tr>
    <tr>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>Cabbagetown, St. James Town</td>
    </tr>
    <tr>
      <td>M4Y</td>
      <td>Downtown Toronto</td>
      <td>Church and Wellesley</td>
    </tr>
    <tr>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront</td>
    </tr>
    <tr>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Ryerson, Garden District</td>
    </tr>
    <tr>
      <td>M5C</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
    </tr>
    <tr>
      <td>M5E</td>
      <td>Downtown Toronto</td>
      <td>Berczy Park</td>
    </tr>
    <tr>
      <td>M5G</td>
      <td>Downtown Toronto</td>
      <td>Central Bay Street</td>
    </tr>
    <tr>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Adelaide, King, Richmond</td>
    </tr>
    <tr>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront East, Toronto Islands, Union Station</td>
    </tr>
    <tr>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Design Exchange, Toronto Dominion Centre</td>
    </tr>
    <tr>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Commerce Court, Victoria Hotel</td>
    </tr>
    <tr>
      <td>M5M</td>
      <td>North York</td>
      <td>Bedford Park, Lawrence Manor East</td>
    </tr>
    <tr>
      <td>M5N</td>
      <td>Central Toronto</td>
      <td>Roselawn</td>
    </tr>
    <tr>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill North, Forest Hill West</td>
    </tr>
    <tr>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>The Annex, North Midtown, Yorkville</td>
    </tr>
    <tr>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>Harbord, University of Toronto</td>
    </tr>
    <tr>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Chinatown, Grange Park, Kensington Market</td>
    </tr>
    <tr>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>CN Tower, Bathurst Quay, Island airport, Harbo...</td>
    </tr>
    <tr>
      <td>M5W</td>
      <td>Downtown Toronto</td>
      <td>Stn A PO Boxes 25 The Esplanade</td>
    </tr>
    <tr>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>First Canadian Place, Underground city</td>
    </tr>
    <tr>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Heights, Lawrence Manor</td>
    </tr>
    <tr>
      <td>M6B</td>
      <td>North York</td>
      <td>Glencairn</td>
    </tr>
    <tr>
      <td>M6C</td>
      <td>York</td>
      <td>Humewood-Cedarvale</td>
    </tr>
    <tr>
      <td>M6E</td>
      <td>York</td>
      <td>Caledonia-Fairbanks</td>
    </tr>
    <tr>
      <td>M6G</td>
      <td>Downtown Toronto</td>
      <td>Christie</td>
    </tr>
    <tr>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dovercourt Village, Dufferin</td>
    </tr>
    <tr>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Little Portugal, Trinity</td>
    </tr>
    <tr>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Brockton, Exhibition Place, Parkdale Village</td>
    </tr>
    <tr>
      <td>M6L</td>
      <td>North York</td>
      <td>Downsview, North Park, Upwood Park</td>
    </tr>
    <tr>
      <td>M6M</td>
      <td>York</td>
      <td>Del Ray, Keelesdale, Mount Dennis, Silverthorn</td>
    </tr>
    <tr>
      <td>M6N</td>
      <td>York</td>
      <td>The Junction North, Runnymede</td>
    </tr>
    <tr>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>High Park, The Junction South</td>
    </tr>
    <tr>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Parkdale, Roncesvalles</td>
    </tr>
    <tr>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Runnymede, Swansea</td>
    </tr>
    <tr>
      <td>M7A</td>
      <td>Queen's Park</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>M7R</td>
      <td>Mississauga</td>
      <td>Canada Post Gateway Processing Centre</td>
    </tr>
    <tr>
      <td>M7Y</td>
      <td>East Toronto</td>
      <td>Business Reply Mail Processing Centre 969 Eastern</td>
    </tr>
    <tr>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Humber Bay Shores, Mimico South, New Toronto</td>
    </tr>
    <tr>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood, Long Branch</td>
    </tr>
    <tr>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>The Kingsway, Montgomery Road, Old Mill North</td>
    </tr>
    <tr>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Humber Bay, King's Mill Park, Kingsway Park So...</td>
    </tr>
    <tr>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South West, Mimico NW, The Queen...</td>
    </tr>
    <tr>
      <td>M9A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park</td>
    </tr>
    <tr>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Cloverdale, Islington, Martin Grove, Princess ...</td>
    </tr>
    <tr>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Bloordale Gardens, Eringate, Markland Wood, Ol...</td>
    </tr>
    <tr>
      <td>M9L</td>
      <td>North York</td>
      <td>Humber Summit</td>
    </tr>
    <tr>
      <td>M9M</td>
      <td>North York</td>
      <td>Emery, Humberlea</td>
    </tr>
    <tr>
      <td>M9N</td>
      <td>York</td>
      <td>Weston</td>
    </tr>
    <tr>
      <td>M9P</td>
      <td>Etobicoke</td>
      <td>Westmount</td>
    </tr>
    <tr>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Kingsview Village, Martin Grove Gardens, Richv...</td>
    </tr>
    <tr>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens, Beaumond Heights, Humbergate, ...</td>
    </tr>
    <tr>
      <td>M9W</td>
      <td>Etobicoke</td>
      <td>Northwest</td>
    </tr>
  </tbody>
</table>
</div>



Including Index number


```python
Y.reset_index(inplace=True)
Y
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postcode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge, Malvern</td>
    </tr>
    <tr>
      <td>1</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek, Rouge Hill, Port Union</td>
    </tr>
    <tr>
      <td>2</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood, Morningside, West Hill</td>
    </tr>
    <tr>
      <td>3</td>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <td>4</td>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
    <tr>
      <td>5</td>
      <td>M1J</td>
      <td>Scarborough</td>
      <td>Scarborough Village</td>
    </tr>
    <tr>
      <td>6</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>East Birchmount Park, Ionview, Kennedy Park</td>
    </tr>
    <tr>
      <td>7</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Clairlea, Golden Mile, Oakridge</td>
    </tr>
    <tr>
      <td>8</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffcrest, Cliffside, Scarborough Village West</td>
    </tr>
    <tr>
      <td>9</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Birch Cliff, Cliffside West</td>
    </tr>
    <tr>
      <td>10</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Dorset Park, Scarborough Town Centre, Wexford ...</td>
    </tr>
    <tr>
      <td>11</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Maryvale, Wexford</td>
    </tr>
    <tr>
      <td>12</td>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
    </tr>
    <tr>
      <td>13</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Clarks Corners, Sullivan, Tam O'Shanter</td>
    </tr>
    <tr>
      <td>14</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North, L'Amoreaux East, Milliken, St...</td>
    </tr>
    <tr>
      <td>15</td>
      <td>M1W</td>
      <td>Scarborough</td>
      <td>L'Amoreaux West</td>
    </tr>
    <tr>
      <td>16</td>
      <td>M1X</td>
      <td>Scarborough</td>
      <td>Upper Rouge</td>
    </tr>
    <tr>
      <td>17</td>
      <td>M2H</td>
      <td>North York</td>
      <td>Hillcrest Village</td>
    </tr>
    <tr>
      <td>18</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Fairview, Henry Farm, Oriole</td>
    </tr>
    <tr>
      <td>19</td>
      <td>M2K</td>
      <td>North York</td>
      <td>Bayview Village</td>
    </tr>
    <tr>
      <td>20</td>
      <td>M2L</td>
      <td>North York</td>
      <td>Silver Hills, York Mills</td>
    </tr>
    <tr>
      <td>21</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Newtonbrook, Willowdale</td>
    </tr>
    <tr>
      <td>22</td>
      <td>M2N</td>
      <td>North York</td>
      <td>Willowdale South</td>
    </tr>
    <tr>
      <td>23</td>
      <td>M2P</td>
      <td>North York</td>
      <td>York Mills West</td>
    </tr>
    <tr>
      <td>24</td>
      <td>M2R</td>
      <td>North York</td>
      <td>Willowdale West</td>
    </tr>
    <tr>
      <td>25</td>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
    </tr>
    <tr>
      <td>26</td>
      <td>M3B</td>
      <td>North York</td>
      <td>Don Mills North</td>
    </tr>
    <tr>
      <td>27</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Flemingdon Park, Don Mills South</td>
    </tr>
    <tr>
      <td>28</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Bathurst Manor, Downsview North, Wilson Heights</td>
    </tr>
    <tr>
      <td>29</td>
      <td>M3J</td>
      <td>North York</td>
      <td>Northwood Park, York University</td>
    </tr>
    <tr>
      <td>30</td>
      <td>M3K</td>
      <td>North York</td>
      <td>CFB Toronto, Downsview East</td>
    </tr>
    <tr>
      <td>31</td>
      <td>M3L</td>
      <td>North York</td>
      <td>Downsview West</td>
    </tr>
    <tr>
      <td>32</td>
      <td>M3M</td>
      <td>North York</td>
      <td>Downsview Central</td>
    </tr>
    <tr>
      <td>33</td>
      <td>M3N</td>
      <td>North York</td>
      <td>Downsview Northwest</td>
    </tr>
    <tr>
      <td>34</td>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
    </tr>
    <tr>
      <td>35</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Woodbine Gardens, Parkview Hill</td>
    </tr>
    <tr>
      <td>36</td>
      <td>M4C</td>
      <td>East York</td>
      <td>Woodbine Heights</td>
    </tr>
    <tr>
      <td>37</td>
      <td>M4E</td>
      <td>East Toronto</td>
      <td>The Beaches</td>
    </tr>
    <tr>
      <td>38</td>
      <td>M4G</td>
      <td>East York</td>
      <td>Leaside</td>
    </tr>
    <tr>
      <td>39</td>
      <td>M4H</td>
      <td>East York</td>
      <td>Thorncliffe Park</td>
    </tr>
    <tr>
      <td>40</td>
      <td>M4J</td>
      <td>East York</td>
      <td>East Toronto</td>
    </tr>
    <tr>
      <td>41</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>The Danforth West, Riverdale</td>
    </tr>
    <tr>
      <td>42</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>The Beaches West, India Bazaar</td>
    </tr>
    <tr>
      <td>43</td>
      <td>M4M</td>
      <td>East Toronto</td>
      <td>Studio District</td>
    </tr>
    <tr>
      <td>44</td>
      <td>M4N</td>
      <td>Central Toronto</td>
      <td>Lawrence Park</td>
    </tr>
    <tr>
      <td>45</td>
      <td>M4P</td>
      <td>Central Toronto</td>
      <td>Davisville North</td>
    </tr>
    <tr>
      <td>46</td>
      <td>M4R</td>
      <td>Central Toronto</td>
      <td>North Toronto West</td>
    </tr>
    <tr>
      <td>47</td>
      <td>M4S</td>
      <td>Central Toronto</td>
      <td>Davisville</td>
    </tr>
    <tr>
      <td>48</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Moore Park, Summerhill East</td>
    </tr>
    <tr>
      <td>49</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Deer Park, Forest Hill SE, Rathnelly, South Hi...</td>
    </tr>
    <tr>
      <td>50</td>
      <td>M4W</td>
      <td>Downtown Toronto</td>
      <td>Rosedale</td>
    </tr>
    <tr>
      <td>51</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>Cabbagetown, St. James Town</td>
    </tr>
    <tr>
      <td>52</td>
      <td>M4Y</td>
      <td>Downtown Toronto</td>
      <td>Church and Wellesley</td>
    </tr>
    <tr>
      <td>53</td>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront</td>
    </tr>
    <tr>
      <td>54</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Ryerson, Garden District</td>
    </tr>
    <tr>
      <td>55</td>
      <td>M5C</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
    </tr>
    <tr>
      <td>56</td>
      <td>M5E</td>
      <td>Downtown Toronto</td>
      <td>Berczy Park</td>
    </tr>
    <tr>
      <td>57</td>
      <td>M5G</td>
      <td>Downtown Toronto</td>
      <td>Central Bay Street</td>
    </tr>
    <tr>
      <td>58</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Adelaide, King, Richmond</td>
    </tr>
    <tr>
      <td>59</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront East, Toronto Islands, Union Station</td>
    </tr>
    <tr>
      <td>60</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Design Exchange, Toronto Dominion Centre</td>
    </tr>
    <tr>
      <td>61</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Commerce Court, Victoria Hotel</td>
    </tr>
    <tr>
      <td>62</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Bedford Park, Lawrence Manor East</td>
    </tr>
    <tr>
      <td>63</td>
      <td>M5N</td>
      <td>Central Toronto</td>
      <td>Roselawn</td>
    </tr>
    <tr>
      <td>64</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill North, Forest Hill West</td>
    </tr>
    <tr>
      <td>65</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>The Annex, North Midtown, Yorkville</td>
    </tr>
    <tr>
      <td>66</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>Harbord, University of Toronto</td>
    </tr>
    <tr>
      <td>67</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Chinatown, Grange Park, Kensington Market</td>
    </tr>
    <tr>
      <td>68</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>CN Tower, Bathurst Quay, Island airport, Harbo...</td>
    </tr>
    <tr>
      <td>69</td>
      <td>M5W</td>
      <td>Downtown Toronto</td>
      <td>Stn A PO Boxes 25 The Esplanade</td>
    </tr>
    <tr>
      <td>70</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>First Canadian Place, Underground city</td>
    </tr>
    <tr>
      <td>71</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Heights, Lawrence Manor</td>
    </tr>
    <tr>
      <td>72</td>
      <td>M6B</td>
      <td>North York</td>
      <td>Glencairn</td>
    </tr>
    <tr>
      <td>73</td>
      <td>M6C</td>
      <td>York</td>
      <td>Humewood-Cedarvale</td>
    </tr>
    <tr>
      <td>74</td>
      <td>M6E</td>
      <td>York</td>
      <td>Caledonia-Fairbanks</td>
    </tr>
    <tr>
      <td>75</td>
      <td>M6G</td>
      <td>Downtown Toronto</td>
      <td>Christie</td>
    </tr>
    <tr>
      <td>76</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dovercourt Village, Dufferin</td>
    </tr>
    <tr>
      <td>77</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Little Portugal, Trinity</td>
    </tr>
    <tr>
      <td>78</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Brockton, Exhibition Place, Parkdale Village</td>
    </tr>
    <tr>
      <td>79</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Downsview, North Park, Upwood Park</td>
    </tr>
    <tr>
      <td>80</td>
      <td>M6M</td>
      <td>York</td>
      <td>Del Ray, Keelesdale, Mount Dennis, Silverthorn</td>
    </tr>
    <tr>
      <td>81</td>
      <td>M6N</td>
      <td>York</td>
      <td>The Junction North, Runnymede</td>
    </tr>
    <tr>
      <td>82</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>High Park, The Junction South</td>
    </tr>
    <tr>
      <td>83</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Parkdale, Roncesvalles</td>
    </tr>
    <tr>
      <td>84</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Runnymede, Swansea</td>
    </tr>
    <tr>
      <td>85</td>
      <td>M7A</td>
      <td>Queen's Park</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <td>86</td>
      <td>M7R</td>
      <td>Mississauga</td>
      <td>Canada Post Gateway Processing Centre</td>
    </tr>
    <tr>
      <td>87</td>
      <td>M7Y</td>
      <td>East Toronto</td>
      <td>Business Reply Mail Processing Centre 969 Eastern</td>
    </tr>
    <tr>
      <td>88</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Humber Bay Shores, Mimico South, New Toronto</td>
    </tr>
    <tr>
      <td>89</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood, Long Branch</td>
    </tr>
    <tr>
      <td>90</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>The Kingsway, Montgomery Road, Old Mill North</td>
    </tr>
    <tr>
      <td>91</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Humber Bay, King's Mill Park, Kingsway Park So...</td>
    </tr>
    <tr>
      <td>92</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South West, Mimico NW, The Queen...</td>
    </tr>
    <tr>
      <td>93</td>
      <td>M9A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park</td>
    </tr>
    <tr>
      <td>94</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Cloverdale, Islington, Martin Grove, Princess ...</td>
    </tr>
    <tr>
      <td>95</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Bloordale Gardens, Eringate, Markland Wood, Ol...</td>
    </tr>
    <tr>
      <td>96</td>
      <td>M9L</td>
      <td>North York</td>
      <td>Humber Summit</td>
    </tr>
    <tr>
      <td>97</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Emery, Humberlea</td>
    </tr>
    <tr>
      <td>98</td>
      <td>M9N</td>
      <td>York</td>
      <td>Weston</td>
    </tr>
    <tr>
      <td>99</td>
      <td>M9P</td>
      <td>Etobicoke</td>
      <td>Westmount</td>
    </tr>
    <tr>
      <td>100</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Kingsview Village, Martin Grove Gardens, Richv...</td>
    </tr>
    <tr>
      <td>101</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens, Beaumond Heights, Humbergate, ...</td>
    </tr>
    <tr>
      <td>102</td>
      <td>M9W</td>
      <td>Etobicoke</td>
      <td>Northwest</td>
    </tr>
  </tbody>
</table>
</div>



## Setting neighborhood the same as the "borough" for  *Not assigned* neighborhood


```python
Y.loc[(Y.Neighbourhood == 'Not assigned'),'Neighbourhood']='Queen\'s Park'
Y


```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postcode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge, Malvern</td>
    </tr>
    <tr>
      <td>1</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek, Rouge Hill, Port Union</td>
    </tr>
    <tr>
      <td>2</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood, Morningside, West Hill</td>
    </tr>
    <tr>
      <td>3</td>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <td>4</td>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
    <tr>
      <td>5</td>
      <td>M1J</td>
      <td>Scarborough</td>
      <td>Scarborough Village</td>
    </tr>
    <tr>
      <td>6</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>East Birchmount Park, Ionview, Kennedy Park</td>
    </tr>
    <tr>
      <td>7</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Clairlea, Golden Mile, Oakridge</td>
    </tr>
    <tr>
      <td>8</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffcrest, Cliffside, Scarborough Village West</td>
    </tr>
    <tr>
      <td>9</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Birch Cliff, Cliffside West</td>
    </tr>
    <tr>
      <td>10</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Dorset Park, Scarborough Town Centre, Wexford ...</td>
    </tr>
    <tr>
      <td>11</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Maryvale, Wexford</td>
    </tr>
    <tr>
      <td>12</td>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
    </tr>
    <tr>
      <td>13</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Clarks Corners, Sullivan, Tam O'Shanter</td>
    </tr>
    <tr>
      <td>14</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North, L'Amoreaux East, Milliken, St...</td>
    </tr>
    <tr>
      <td>15</td>
      <td>M1W</td>
      <td>Scarborough</td>
      <td>L'Amoreaux West</td>
    </tr>
    <tr>
      <td>16</td>
      <td>M1X</td>
      <td>Scarborough</td>
      <td>Upper Rouge</td>
    </tr>
    <tr>
      <td>17</td>
      <td>M2H</td>
      <td>North York</td>
      <td>Hillcrest Village</td>
    </tr>
    <tr>
      <td>18</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Fairview, Henry Farm, Oriole</td>
    </tr>
    <tr>
      <td>19</td>
      <td>M2K</td>
      <td>North York</td>
      <td>Bayview Village</td>
    </tr>
    <tr>
      <td>20</td>
      <td>M2L</td>
      <td>North York</td>
      <td>Silver Hills, York Mills</td>
    </tr>
    <tr>
      <td>21</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Newtonbrook, Willowdale</td>
    </tr>
    <tr>
      <td>22</td>
      <td>M2N</td>
      <td>North York</td>
      <td>Willowdale South</td>
    </tr>
    <tr>
      <td>23</td>
      <td>M2P</td>
      <td>North York</td>
      <td>York Mills West</td>
    </tr>
    <tr>
      <td>24</td>
      <td>M2R</td>
      <td>North York</td>
      <td>Willowdale West</td>
    </tr>
    <tr>
      <td>25</td>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
    </tr>
    <tr>
      <td>26</td>
      <td>M3B</td>
      <td>North York</td>
      <td>Don Mills North</td>
    </tr>
    <tr>
      <td>27</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Flemingdon Park, Don Mills South</td>
    </tr>
    <tr>
      <td>28</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Bathurst Manor, Downsview North, Wilson Heights</td>
    </tr>
    <tr>
      <td>29</td>
      <td>M3J</td>
      <td>North York</td>
      <td>Northwood Park, York University</td>
    </tr>
    <tr>
      <td>30</td>
      <td>M3K</td>
      <td>North York</td>
      <td>CFB Toronto, Downsview East</td>
    </tr>
    <tr>
      <td>31</td>
      <td>M3L</td>
      <td>North York</td>
      <td>Downsview West</td>
    </tr>
    <tr>
      <td>32</td>
      <td>M3M</td>
      <td>North York</td>
      <td>Downsview Central</td>
    </tr>
    <tr>
      <td>33</td>
      <td>M3N</td>
      <td>North York</td>
      <td>Downsview Northwest</td>
    </tr>
    <tr>
      <td>34</td>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
    </tr>
    <tr>
      <td>35</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Woodbine Gardens, Parkview Hill</td>
    </tr>
    <tr>
      <td>36</td>
      <td>M4C</td>
      <td>East York</td>
      <td>Woodbine Heights</td>
    </tr>
    <tr>
      <td>37</td>
      <td>M4E</td>
      <td>East Toronto</td>
      <td>The Beaches</td>
    </tr>
    <tr>
      <td>38</td>
      <td>M4G</td>
      <td>East York</td>
      <td>Leaside</td>
    </tr>
    <tr>
      <td>39</td>
      <td>M4H</td>
      <td>East York</td>
      <td>Thorncliffe Park</td>
    </tr>
    <tr>
      <td>40</td>
      <td>M4J</td>
      <td>East York</td>
      <td>East Toronto</td>
    </tr>
    <tr>
      <td>41</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>The Danforth West, Riverdale</td>
    </tr>
    <tr>
      <td>42</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>The Beaches West, India Bazaar</td>
    </tr>
    <tr>
      <td>43</td>
      <td>M4M</td>
      <td>East Toronto</td>
      <td>Studio District</td>
    </tr>
    <tr>
      <td>44</td>
      <td>M4N</td>
      <td>Central Toronto</td>
      <td>Lawrence Park</td>
    </tr>
    <tr>
      <td>45</td>
      <td>M4P</td>
      <td>Central Toronto</td>
      <td>Davisville North</td>
    </tr>
    <tr>
      <td>46</td>
      <td>M4R</td>
      <td>Central Toronto</td>
      <td>North Toronto West</td>
    </tr>
    <tr>
      <td>47</td>
      <td>M4S</td>
      <td>Central Toronto</td>
      <td>Davisville</td>
    </tr>
    <tr>
      <td>48</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Moore Park, Summerhill East</td>
    </tr>
    <tr>
      <td>49</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Deer Park, Forest Hill SE, Rathnelly, South Hi...</td>
    </tr>
    <tr>
      <td>50</td>
      <td>M4W</td>
      <td>Downtown Toronto</td>
      <td>Rosedale</td>
    </tr>
    <tr>
      <td>51</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>Cabbagetown, St. James Town</td>
    </tr>
    <tr>
      <td>52</td>
      <td>M4Y</td>
      <td>Downtown Toronto</td>
      <td>Church and Wellesley</td>
    </tr>
    <tr>
      <td>53</td>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront</td>
    </tr>
    <tr>
      <td>54</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Ryerson, Garden District</td>
    </tr>
    <tr>
      <td>55</td>
      <td>M5C</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
    </tr>
    <tr>
      <td>56</td>
      <td>M5E</td>
      <td>Downtown Toronto</td>
      <td>Berczy Park</td>
    </tr>
    <tr>
      <td>57</td>
      <td>M5G</td>
      <td>Downtown Toronto</td>
      <td>Central Bay Street</td>
    </tr>
    <tr>
      <td>58</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Adelaide, King, Richmond</td>
    </tr>
    <tr>
      <td>59</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront East, Toronto Islands, Union Station</td>
    </tr>
    <tr>
      <td>60</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Design Exchange, Toronto Dominion Centre</td>
    </tr>
    <tr>
      <td>61</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Commerce Court, Victoria Hotel</td>
    </tr>
    <tr>
      <td>62</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Bedford Park, Lawrence Manor East</td>
    </tr>
    <tr>
      <td>63</td>
      <td>M5N</td>
      <td>Central Toronto</td>
      <td>Roselawn</td>
    </tr>
    <tr>
      <td>64</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill North, Forest Hill West</td>
    </tr>
    <tr>
      <td>65</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>The Annex, North Midtown, Yorkville</td>
    </tr>
    <tr>
      <td>66</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>Harbord, University of Toronto</td>
    </tr>
    <tr>
      <td>67</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Chinatown, Grange Park, Kensington Market</td>
    </tr>
    <tr>
      <td>68</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>CN Tower, Bathurst Quay, Island airport, Harbo...</td>
    </tr>
    <tr>
      <td>69</td>
      <td>M5W</td>
      <td>Downtown Toronto</td>
      <td>Stn A PO Boxes 25 The Esplanade</td>
    </tr>
    <tr>
      <td>70</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>First Canadian Place, Underground city</td>
    </tr>
    <tr>
      <td>71</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Heights, Lawrence Manor</td>
    </tr>
    <tr>
      <td>72</td>
      <td>M6B</td>
      <td>North York</td>
      <td>Glencairn</td>
    </tr>
    <tr>
      <td>73</td>
      <td>M6C</td>
      <td>York</td>
      <td>Humewood-Cedarvale</td>
    </tr>
    <tr>
      <td>74</td>
      <td>M6E</td>
      <td>York</td>
      <td>Caledonia-Fairbanks</td>
    </tr>
    <tr>
      <td>75</td>
      <td>M6G</td>
      <td>Downtown Toronto</td>
      <td>Christie</td>
    </tr>
    <tr>
      <td>76</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dovercourt Village, Dufferin</td>
    </tr>
    <tr>
      <td>77</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Little Portugal, Trinity</td>
    </tr>
    <tr>
      <td>78</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Brockton, Exhibition Place, Parkdale Village</td>
    </tr>
    <tr>
      <td>79</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Downsview, North Park, Upwood Park</td>
    </tr>
    <tr>
      <td>80</td>
      <td>M6M</td>
      <td>York</td>
      <td>Del Ray, Keelesdale, Mount Dennis, Silverthorn</td>
    </tr>
    <tr>
      <td>81</td>
      <td>M6N</td>
      <td>York</td>
      <td>The Junction North, Runnymede</td>
    </tr>
    <tr>
      <td>82</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>High Park, The Junction South</td>
    </tr>
    <tr>
      <td>83</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Parkdale, Roncesvalles</td>
    </tr>
    <tr>
      <td>84</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Runnymede, Swansea</td>
    </tr>
    <tr>
      <td>85</td>
      <td>M7A</td>
      <td>Queen's Park</td>
      <td>Queen's Park</td>
    </tr>
    <tr>
      <td>86</td>
      <td>M7R</td>
      <td>Mississauga</td>
      <td>Canada Post Gateway Processing Centre</td>
    </tr>
    <tr>
      <td>87</td>
      <td>M7Y</td>
      <td>East Toronto</td>
      <td>Business Reply Mail Processing Centre 969 Eastern</td>
    </tr>
    <tr>
      <td>88</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Humber Bay Shores, Mimico South, New Toronto</td>
    </tr>
    <tr>
      <td>89</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood, Long Branch</td>
    </tr>
    <tr>
      <td>90</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>The Kingsway, Montgomery Road, Old Mill North</td>
    </tr>
    <tr>
      <td>91</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Humber Bay, King's Mill Park, Kingsway Park So...</td>
    </tr>
    <tr>
      <td>92</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South West, Mimico NW, The Queen...</td>
    </tr>
    <tr>
      <td>93</td>
      <td>M9A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park</td>
    </tr>
    <tr>
      <td>94</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Cloverdale, Islington, Martin Grove, Princess ...</td>
    </tr>
    <tr>
      <td>95</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Bloordale Gardens, Eringate, Markland Wood, Ol...</td>
    </tr>
    <tr>
      <td>96</td>
      <td>M9L</td>
      <td>North York</td>
      <td>Humber Summit</td>
    </tr>
    <tr>
      <td>97</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Emery, Humberlea</td>
    </tr>
    <tr>
      <td>98</td>
      <td>M9N</td>
      <td>York</td>
      <td>Weston</td>
    </tr>
    <tr>
      <td>99</td>
      <td>M9P</td>
      <td>Etobicoke</td>
      <td>Westmount</td>
    </tr>
    <tr>
      <td>100</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Kingsview Village, Martin Grove Gardens, Richv...</td>
    </tr>
    <tr>
      <td>101</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens, Beaumond Heights, Humbergate, ...</td>
    </tr>
    <tr>
      <td>102</td>
      <td>M9W</td>
      <td>Etobicoke</td>
      <td>Northwest</td>
    </tr>
  </tbody>
</table>
</div>



# Shape


```python
Y.shape
```




    (103, 3)



## Importing Geospatial Data


```python
geo=pd.read_csv("D:\IBM Data Science Professional Certificate\Capstone Project\week3\\Geospatial_Coordinates.csv")
```


```python
geo.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postal Code</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>M1B</td>
      <td>43.806686</td>
      <td>-79.194353</td>
    </tr>
    <tr>
      <td>1</td>
      <td>M1C</td>
      <td>43.784535</td>
      <td>-79.160497</td>
    </tr>
    <tr>
      <td>2</td>
      <td>M1E</td>
      <td>43.763573</td>
      <td>-79.188711</td>
    </tr>
    <tr>
      <td>3</td>
      <td>M1G</td>
      <td>43.770992</td>
      <td>-79.216917</td>
    </tr>
    <tr>
      <td>4</td>
      <td>M1H</td>
      <td>43.773136</td>
      <td>-79.239476</td>
    </tr>
  </tbody>
</table>
</div>



## Concatenating two tables


```python
DataFrame= pd.concat([Y, geo],axis=1)
DataFrame
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postcode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>Postal Code</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge, Malvern</td>
      <td>M1B</td>
      <td>43.806686</td>
      <td>-79.194353</td>
    </tr>
    <tr>
      <td>1</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek, Rouge Hill, Port Union</td>
      <td>M1C</td>
      <td>43.784535</td>
      <td>-79.160497</td>
    </tr>
    <tr>
      <td>2</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood, Morningside, West Hill</td>
      <td>M1E</td>
      <td>43.763573</td>
      <td>-79.188711</td>
    </tr>
    <tr>
      <td>3</td>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>M1G</td>
      <td>43.770992</td>
      <td>-79.216917</td>
    </tr>
    <tr>
      <td>4</td>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>M1H</td>
      <td>43.773136</td>
      <td>-79.239476</td>
    </tr>
    <tr>
      <td>5</td>
      <td>M1J</td>
      <td>Scarborough</td>
      <td>Scarborough Village</td>
      <td>M1J</td>
      <td>43.744734</td>
      <td>-79.239476</td>
    </tr>
    <tr>
      <td>6</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>East Birchmount Park, Ionview, Kennedy Park</td>
      <td>M1K</td>
      <td>43.727929</td>
      <td>-79.262029</td>
    </tr>
    <tr>
      <td>7</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Clairlea, Golden Mile, Oakridge</td>
      <td>M1L</td>
      <td>43.711112</td>
      <td>-79.284577</td>
    </tr>
    <tr>
      <td>8</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffcrest, Cliffside, Scarborough Village West</td>
      <td>M1M</td>
      <td>43.716316</td>
      <td>-79.239476</td>
    </tr>
    <tr>
      <td>9</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Birch Cliff, Cliffside West</td>
      <td>M1N</td>
      <td>43.692657</td>
      <td>-79.264848</td>
    </tr>
    <tr>
      <td>10</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Dorset Park, Scarborough Town Centre, Wexford ...</td>
      <td>M1P</td>
      <td>43.757410</td>
      <td>-79.273304</td>
    </tr>
    <tr>
      <td>11</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Maryvale, Wexford</td>
      <td>M1R</td>
      <td>43.750072</td>
      <td>-79.295849</td>
    </tr>
    <tr>
      <td>12</td>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
      <td>M1S</td>
      <td>43.794200</td>
      <td>-79.262029</td>
    </tr>
    <tr>
      <td>13</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Clarks Corners, Sullivan, Tam O'Shanter</td>
      <td>M1T</td>
      <td>43.781638</td>
      <td>-79.304302</td>
    </tr>
    <tr>
      <td>14</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North, L'Amoreaux East, Milliken, St...</td>
      <td>M1V</td>
      <td>43.815252</td>
      <td>-79.284577</td>
    </tr>
    <tr>
      <td>15</td>
      <td>M1W</td>
      <td>Scarborough</td>
      <td>L'Amoreaux West</td>
      <td>M1W</td>
      <td>43.799525</td>
      <td>-79.318389</td>
    </tr>
    <tr>
      <td>16</td>
      <td>M1X</td>
      <td>Scarborough</td>
      <td>Upper Rouge</td>
      <td>M1X</td>
      <td>43.836125</td>
      <td>-79.205636</td>
    </tr>
    <tr>
      <td>17</td>
      <td>M2H</td>
      <td>North York</td>
      <td>Hillcrest Village</td>
      <td>M2H</td>
      <td>43.803762</td>
      <td>-79.363452</td>
    </tr>
    <tr>
      <td>18</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Fairview, Henry Farm, Oriole</td>
      <td>M2J</td>
      <td>43.778517</td>
      <td>-79.346556</td>
    </tr>
    <tr>
      <td>19</td>
      <td>M2K</td>
      <td>North York</td>
      <td>Bayview Village</td>
      <td>M2K</td>
      <td>43.786947</td>
      <td>-79.385975</td>
    </tr>
    <tr>
      <td>20</td>
      <td>M2L</td>
      <td>North York</td>
      <td>Silver Hills, York Mills</td>
      <td>M2L</td>
      <td>43.757490</td>
      <td>-79.374714</td>
    </tr>
    <tr>
      <td>21</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Newtonbrook, Willowdale</td>
      <td>M2M</td>
      <td>43.789053</td>
      <td>-79.408493</td>
    </tr>
    <tr>
      <td>22</td>
      <td>M2N</td>
      <td>North York</td>
      <td>Willowdale South</td>
      <td>M2N</td>
      <td>43.770120</td>
      <td>-79.408493</td>
    </tr>
    <tr>
      <td>23</td>
      <td>M2P</td>
      <td>North York</td>
      <td>York Mills West</td>
      <td>M2P</td>
      <td>43.752758</td>
      <td>-79.400049</td>
    </tr>
    <tr>
      <td>24</td>
      <td>M2R</td>
      <td>North York</td>
      <td>Willowdale West</td>
      <td>M2R</td>
      <td>43.782736</td>
      <td>-79.442259</td>
    </tr>
    <tr>
      <td>25</td>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
      <td>M3A</td>
      <td>43.753259</td>
      <td>-79.329656</td>
    </tr>
    <tr>
      <td>26</td>
      <td>M3B</td>
      <td>North York</td>
      <td>Don Mills North</td>
      <td>M3B</td>
      <td>43.745906</td>
      <td>-79.352188</td>
    </tr>
    <tr>
      <td>27</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Flemingdon Park, Don Mills South</td>
      <td>M3C</td>
      <td>43.725900</td>
      <td>-79.340923</td>
    </tr>
    <tr>
      <td>28</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Bathurst Manor, Downsview North, Wilson Heights</td>
      <td>M3H</td>
      <td>43.754328</td>
      <td>-79.442259</td>
    </tr>
    <tr>
      <td>29</td>
      <td>M3J</td>
      <td>North York</td>
      <td>Northwood Park, York University</td>
      <td>M3J</td>
      <td>43.767980</td>
      <td>-79.487262</td>
    </tr>
    <tr>
      <td>30</td>
      <td>M3K</td>
      <td>North York</td>
      <td>CFB Toronto, Downsview East</td>
      <td>M3K</td>
      <td>43.737473</td>
      <td>-79.464763</td>
    </tr>
    <tr>
      <td>31</td>
      <td>M3L</td>
      <td>North York</td>
      <td>Downsview West</td>
      <td>M3L</td>
      <td>43.739015</td>
      <td>-79.506944</td>
    </tr>
    <tr>
      <td>32</td>
      <td>M3M</td>
      <td>North York</td>
      <td>Downsview Central</td>
      <td>M3M</td>
      <td>43.728496</td>
      <td>-79.495697</td>
    </tr>
    <tr>
      <td>33</td>
      <td>M3N</td>
      <td>North York</td>
      <td>Downsview Northwest</td>
      <td>M3N</td>
      <td>43.761631</td>
      <td>-79.520999</td>
    </tr>
    <tr>
      <td>34</td>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
      <td>M4A</td>
      <td>43.725882</td>
      <td>-79.315572</td>
    </tr>
    <tr>
      <td>35</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Woodbine Gardens, Parkview Hill</td>
      <td>M4B</td>
      <td>43.706397</td>
      <td>-79.309937</td>
    </tr>
    <tr>
      <td>36</td>
      <td>M4C</td>
      <td>East York</td>
      <td>Woodbine Heights</td>
      <td>M4C</td>
      <td>43.695344</td>
      <td>-79.318389</td>
    </tr>
    <tr>
      <td>37</td>
      <td>M4E</td>
      <td>East Toronto</td>
      <td>The Beaches</td>
      <td>M4E</td>
      <td>43.676357</td>
      <td>-79.293031</td>
    </tr>
    <tr>
      <td>38</td>
      <td>M4G</td>
      <td>East York</td>
      <td>Leaside</td>
      <td>M4G</td>
      <td>43.709060</td>
      <td>-79.363452</td>
    </tr>
    <tr>
      <td>39</td>
      <td>M4H</td>
      <td>East York</td>
      <td>Thorncliffe Park</td>
      <td>M4H</td>
      <td>43.705369</td>
      <td>-79.349372</td>
    </tr>
    <tr>
      <td>40</td>
      <td>M4J</td>
      <td>East York</td>
      <td>East Toronto</td>
      <td>M4J</td>
      <td>43.685347</td>
      <td>-79.338106</td>
    </tr>
    <tr>
      <td>41</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>The Danforth West, Riverdale</td>
      <td>M4K</td>
      <td>43.679557</td>
      <td>-79.352188</td>
    </tr>
    <tr>
      <td>42</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>The Beaches West, India Bazaar</td>
      <td>M4L</td>
      <td>43.668999</td>
      <td>-79.315572</td>
    </tr>
    <tr>
      <td>43</td>
      <td>M4M</td>
      <td>East Toronto</td>
      <td>Studio District</td>
      <td>M4M</td>
      <td>43.659526</td>
      <td>-79.340923</td>
    </tr>
    <tr>
      <td>44</td>
      <td>M4N</td>
      <td>Central Toronto</td>
      <td>Lawrence Park</td>
      <td>M4N</td>
      <td>43.728020</td>
      <td>-79.388790</td>
    </tr>
    <tr>
      <td>45</td>
      <td>M4P</td>
      <td>Central Toronto</td>
      <td>Davisville North</td>
      <td>M4P</td>
      <td>43.712751</td>
      <td>-79.390197</td>
    </tr>
    <tr>
      <td>46</td>
      <td>M4R</td>
      <td>Central Toronto</td>
      <td>North Toronto West</td>
      <td>M4R</td>
      <td>43.715383</td>
      <td>-79.405678</td>
    </tr>
    <tr>
      <td>47</td>
      <td>M4S</td>
      <td>Central Toronto</td>
      <td>Davisville</td>
      <td>M4S</td>
      <td>43.704324</td>
      <td>-79.388790</td>
    </tr>
    <tr>
      <td>48</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Moore Park, Summerhill East</td>
      <td>M4T</td>
      <td>43.689574</td>
      <td>-79.383160</td>
    </tr>
    <tr>
      <td>49</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Deer Park, Forest Hill SE, Rathnelly, South Hi...</td>
      <td>M4V</td>
      <td>43.686412</td>
      <td>-79.400049</td>
    </tr>
    <tr>
      <td>50</td>
      <td>M4W</td>
      <td>Downtown Toronto</td>
      <td>Rosedale</td>
      <td>M4W</td>
      <td>43.679563</td>
      <td>-79.377529</td>
    </tr>
    <tr>
      <td>51</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>Cabbagetown, St. James Town</td>
      <td>M4X</td>
      <td>43.667967</td>
      <td>-79.367675</td>
    </tr>
    <tr>
      <td>52</td>
      <td>M4Y</td>
      <td>Downtown Toronto</td>
      <td>Church and Wellesley</td>
      <td>M4Y</td>
      <td>43.665860</td>
      <td>-79.383160</td>
    </tr>
    <tr>
      <td>53</td>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront</td>
      <td>M5A</td>
      <td>43.654260</td>
      <td>-79.360636</td>
    </tr>
    <tr>
      <td>54</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Ryerson, Garden District</td>
      <td>M5B</td>
      <td>43.657162</td>
      <td>-79.378937</td>
    </tr>
    <tr>
      <td>55</td>
      <td>M5C</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
      <td>M5C</td>
      <td>43.651494</td>
      <td>-79.375418</td>
    </tr>
    <tr>
      <td>56</td>
      <td>M5E</td>
      <td>Downtown Toronto</td>
      <td>Berczy Park</td>
      <td>M5E</td>
      <td>43.644771</td>
      <td>-79.373306</td>
    </tr>
    <tr>
      <td>57</td>
      <td>M5G</td>
      <td>Downtown Toronto</td>
      <td>Central Bay Street</td>
      <td>M5G</td>
      <td>43.657952</td>
      <td>-79.387383</td>
    </tr>
    <tr>
      <td>58</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Adelaide, King, Richmond</td>
      <td>M5H</td>
      <td>43.650571</td>
      <td>-79.384568</td>
    </tr>
    <tr>
      <td>59</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront East, Toronto Islands, Union Station</td>
      <td>M5J</td>
      <td>43.640816</td>
      <td>-79.381752</td>
    </tr>
    <tr>
      <td>60</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Design Exchange, Toronto Dominion Centre</td>
      <td>M5K</td>
      <td>43.647177</td>
      <td>-79.381576</td>
    </tr>
    <tr>
      <td>61</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Commerce Court, Victoria Hotel</td>
      <td>M5L</td>
      <td>43.648198</td>
      <td>-79.379817</td>
    </tr>
    <tr>
      <td>62</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Bedford Park, Lawrence Manor East</td>
      <td>M5M</td>
      <td>43.733283</td>
      <td>-79.419750</td>
    </tr>
    <tr>
      <td>63</td>
      <td>M5N</td>
      <td>Central Toronto</td>
      <td>Roselawn</td>
      <td>M5N</td>
      <td>43.711695</td>
      <td>-79.416936</td>
    </tr>
    <tr>
      <td>64</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill North, Forest Hill West</td>
      <td>M5P</td>
      <td>43.696948</td>
      <td>-79.411307</td>
    </tr>
    <tr>
      <td>65</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>The Annex, North Midtown, Yorkville</td>
      <td>M5R</td>
      <td>43.672710</td>
      <td>-79.405678</td>
    </tr>
    <tr>
      <td>66</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>Harbord, University of Toronto</td>
      <td>M5S</td>
      <td>43.662696</td>
      <td>-79.400049</td>
    </tr>
    <tr>
      <td>67</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Chinatown, Grange Park, Kensington Market</td>
      <td>M5T</td>
      <td>43.653206</td>
      <td>-79.400049</td>
    </tr>
    <tr>
      <td>68</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>CN Tower, Bathurst Quay, Island airport, Harbo...</td>
      <td>M5V</td>
      <td>43.628947</td>
      <td>-79.394420</td>
    </tr>
    <tr>
      <td>69</td>
      <td>M5W</td>
      <td>Downtown Toronto</td>
      <td>Stn A PO Boxes 25 The Esplanade</td>
      <td>M5W</td>
      <td>43.646435</td>
      <td>-79.374846</td>
    </tr>
    <tr>
      <td>70</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>First Canadian Place, Underground city</td>
      <td>M5X</td>
      <td>43.648429</td>
      <td>-79.382280</td>
    </tr>
    <tr>
      <td>71</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Heights, Lawrence Manor</td>
      <td>M6A</td>
      <td>43.718518</td>
      <td>-79.464763</td>
    </tr>
    <tr>
      <td>72</td>
      <td>M6B</td>
      <td>North York</td>
      <td>Glencairn</td>
      <td>M6B</td>
      <td>43.709577</td>
      <td>-79.445073</td>
    </tr>
    <tr>
      <td>73</td>
      <td>M6C</td>
      <td>York</td>
      <td>Humewood-Cedarvale</td>
      <td>M6C</td>
      <td>43.693781</td>
      <td>-79.428191</td>
    </tr>
    <tr>
      <td>74</td>
      <td>M6E</td>
      <td>York</td>
      <td>Caledonia-Fairbanks</td>
      <td>M6E</td>
      <td>43.689026</td>
      <td>-79.453512</td>
    </tr>
    <tr>
      <td>75</td>
      <td>M6G</td>
      <td>Downtown Toronto</td>
      <td>Christie</td>
      <td>M6G</td>
      <td>43.669542</td>
      <td>-79.422564</td>
    </tr>
    <tr>
      <td>76</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dovercourt Village, Dufferin</td>
      <td>M6H</td>
      <td>43.669005</td>
      <td>-79.442259</td>
    </tr>
    <tr>
      <td>77</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Little Portugal, Trinity</td>
      <td>M6J</td>
      <td>43.647927</td>
      <td>-79.419750</td>
    </tr>
    <tr>
      <td>78</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Brockton, Exhibition Place, Parkdale Village</td>
      <td>M6K</td>
      <td>43.636847</td>
      <td>-79.428191</td>
    </tr>
    <tr>
      <td>79</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Downsview, North Park, Upwood Park</td>
      <td>M6L</td>
      <td>43.713756</td>
      <td>-79.490074</td>
    </tr>
    <tr>
      <td>80</td>
      <td>M6M</td>
      <td>York</td>
      <td>Del Ray, Keelesdale, Mount Dennis, Silverthorn</td>
      <td>M6M</td>
      <td>43.691116</td>
      <td>-79.476013</td>
    </tr>
    <tr>
      <td>81</td>
      <td>M6N</td>
      <td>York</td>
      <td>The Junction North, Runnymede</td>
      <td>M6N</td>
      <td>43.673185</td>
      <td>-79.487262</td>
    </tr>
    <tr>
      <td>82</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>High Park, The Junction South</td>
      <td>M6P</td>
      <td>43.661608</td>
      <td>-79.464763</td>
    </tr>
    <tr>
      <td>83</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Parkdale, Roncesvalles</td>
      <td>M6R</td>
      <td>43.648960</td>
      <td>-79.456325</td>
    </tr>
    <tr>
      <td>84</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Runnymede, Swansea</td>
      <td>M6S</td>
      <td>43.651571</td>
      <td>-79.484450</td>
    </tr>
    <tr>
      <td>85</td>
      <td>M7A</td>
      <td>Queen's Park</td>
      <td>Queen's Park</td>
      <td>M7A</td>
      <td>43.662301</td>
      <td>-79.389494</td>
    </tr>
    <tr>
      <td>86</td>
      <td>M7R</td>
      <td>Mississauga</td>
      <td>Canada Post Gateway Processing Centre</td>
      <td>M7R</td>
      <td>43.636966</td>
      <td>-79.615819</td>
    </tr>
    <tr>
      <td>87</td>
      <td>M7Y</td>
      <td>East Toronto</td>
      <td>Business Reply Mail Processing Centre 969 Eastern</td>
      <td>M7Y</td>
      <td>43.662744</td>
      <td>-79.321558</td>
    </tr>
    <tr>
      <td>88</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Humber Bay Shores, Mimico South, New Toronto</td>
      <td>M8V</td>
      <td>43.605647</td>
      <td>-79.501321</td>
    </tr>
    <tr>
      <td>89</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood, Long Branch</td>
      <td>M8W</td>
      <td>43.602414</td>
      <td>-79.543484</td>
    </tr>
    <tr>
      <td>90</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>The Kingsway, Montgomery Road, Old Mill North</td>
      <td>M8X</td>
      <td>43.653654</td>
      <td>-79.506944</td>
    </tr>
    <tr>
      <td>91</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Humber Bay, King's Mill Park, Kingsway Park So...</td>
      <td>M8Y</td>
      <td>43.636258</td>
      <td>-79.498509</td>
    </tr>
    <tr>
      <td>92</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South West, Mimico NW, The Queen...</td>
      <td>M8Z</td>
      <td>43.628841</td>
      <td>-79.520999</td>
    </tr>
    <tr>
      <td>93</td>
      <td>M9A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park</td>
      <td>M9A</td>
      <td>43.667856</td>
      <td>-79.532242</td>
    </tr>
    <tr>
      <td>94</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Cloverdale, Islington, Martin Grove, Princess ...</td>
      <td>M9B</td>
      <td>43.650943</td>
      <td>-79.554724</td>
    </tr>
    <tr>
      <td>95</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Bloordale Gardens, Eringate, Markland Wood, Ol...</td>
      <td>M9C</td>
      <td>43.643515</td>
      <td>-79.577201</td>
    </tr>
    <tr>
      <td>96</td>
      <td>M9L</td>
      <td>North York</td>
      <td>Humber Summit</td>
      <td>M9L</td>
      <td>43.756303</td>
      <td>-79.565963</td>
    </tr>
    <tr>
      <td>97</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Emery, Humberlea</td>
      <td>M9M</td>
      <td>43.724766</td>
      <td>-79.532242</td>
    </tr>
    <tr>
      <td>98</td>
      <td>M9N</td>
      <td>York</td>
      <td>Weston</td>
      <td>M9N</td>
      <td>43.706876</td>
      <td>-79.518188</td>
    </tr>
    <tr>
      <td>99</td>
      <td>M9P</td>
      <td>Etobicoke</td>
      <td>Westmount</td>
      <td>M9P</td>
      <td>43.696319</td>
      <td>-79.532242</td>
    </tr>
    <tr>
      <td>100</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Kingsview Village, Martin Grove Gardens, Richv...</td>
      <td>M9R</td>
      <td>43.688905</td>
      <td>-79.554724</td>
    </tr>
    <tr>
      <td>101</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens, Beaumond Heights, Humbergate, ...</td>
      <td>M9V</td>
      <td>43.739416</td>
      <td>-79.588437</td>
    </tr>
    <tr>
      <td>102</td>
      <td>M9W</td>
      <td>Etobicoke</td>
      <td>Northwest</td>
      <td>M9W</td>
      <td>43.706748</td>
      <td>-79.594054</td>
    </tr>
  </tbody>
</table>
</div>



Desired DataFrame


```python
DataFrame.drop(columns=['Postal Code'],inplace=True)
DataFrame
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postcode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge, Malvern</td>
      <td>43.806686</td>
      <td>-79.194353</td>
    </tr>
    <tr>
      <td>1</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek, Rouge Hill, Port Union</td>
      <td>43.784535</td>
      <td>-79.160497</td>
    </tr>
    <tr>
      <td>2</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood, Morningside, West Hill</td>
      <td>43.763573</td>
      <td>-79.188711</td>
    </tr>
    <tr>
      <td>3</td>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>43.770992</td>
      <td>-79.216917</td>
    </tr>
    <tr>
      <td>4</td>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>43.773136</td>
      <td>-79.239476</td>
    </tr>
    <tr>
      <td>5</td>
      <td>M1J</td>
      <td>Scarborough</td>
      <td>Scarborough Village</td>
      <td>43.744734</td>
      <td>-79.239476</td>
    </tr>
    <tr>
      <td>6</td>
      <td>M1K</td>
      <td>Scarborough</td>
      <td>East Birchmount Park, Ionview, Kennedy Park</td>
      <td>43.727929</td>
      <td>-79.262029</td>
    </tr>
    <tr>
      <td>7</td>
      <td>M1L</td>
      <td>Scarborough</td>
      <td>Clairlea, Golden Mile, Oakridge</td>
      <td>43.711112</td>
      <td>-79.284577</td>
    </tr>
    <tr>
      <td>8</td>
      <td>M1M</td>
      <td>Scarborough</td>
      <td>Cliffcrest, Cliffside, Scarborough Village West</td>
      <td>43.716316</td>
      <td>-79.239476</td>
    </tr>
    <tr>
      <td>9</td>
      <td>M1N</td>
      <td>Scarborough</td>
      <td>Birch Cliff, Cliffside West</td>
      <td>43.692657</td>
      <td>-79.264848</td>
    </tr>
    <tr>
      <td>10</td>
      <td>M1P</td>
      <td>Scarborough</td>
      <td>Dorset Park, Scarborough Town Centre, Wexford ...</td>
      <td>43.757410</td>
      <td>-79.273304</td>
    </tr>
    <tr>
      <td>11</td>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Maryvale, Wexford</td>
      <td>43.750072</td>
      <td>-79.295849</td>
    </tr>
    <tr>
      <td>12</td>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
      <td>43.794200</td>
      <td>-79.262029</td>
    </tr>
    <tr>
      <td>13</td>
      <td>M1T</td>
      <td>Scarborough</td>
      <td>Clarks Corners, Sullivan, Tam O'Shanter</td>
      <td>43.781638</td>
      <td>-79.304302</td>
    </tr>
    <tr>
      <td>14</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North, L'Amoreaux East, Milliken, St...</td>
      <td>43.815252</td>
      <td>-79.284577</td>
    </tr>
    <tr>
      <td>15</td>
      <td>M1W</td>
      <td>Scarborough</td>
      <td>L'Amoreaux West</td>
      <td>43.799525</td>
      <td>-79.318389</td>
    </tr>
    <tr>
      <td>16</td>
      <td>M1X</td>
      <td>Scarborough</td>
      <td>Upper Rouge</td>
      <td>43.836125</td>
      <td>-79.205636</td>
    </tr>
    <tr>
      <td>17</td>
      <td>M2H</td>
      <td>North York</td>
      <td>Hillcrest Village</td>
      <td>43.803762</td>
      <td>-79.363452</td>
    </tr>
    <tr>
      <td>18</td>
      <td>M2J</td>
      <td>North York</td>
      <td>Fairview, Henry Farm, Oriole</td>
      <td>43.778517</td>
      <td>-79.346556</td>
    </tr>
    <tr>
      <td>19</td>
      <td>M2K</td>
      <td>North York</td>
      <td>Bayview Village</td>
      <td>43.786947</td>
      <td>-79.385975</td>
    </tr>
    <tr>
      <td>20</td>
      <td>M2L</td>
      <td>North York</td>
      <td>Silver Hills, York Mills</td>
      <td>43.757490</td>
      <td>-79.374714</td>
    </tr>
    <tr>
      <td>21</td>
      <td>M2M</td>
      <td>North York</td>
      <td>Newtonbrook, Willowdale</td>
      <td>43.789053</td>
      <td>-79.408493</td>
    </tr>
    <tr>
      <td>22</td>
      <td>M2N</td>
      <td>North York</td>
      <td>Willowdale South</td>
      <td>43.770120</td>
      <td>-79.408493</td>
    </tr>
    <tr>
      <td>23</td>
      <td>M2P</td>
      <td>North York</td>
      <td>York Mills West</td>
      <td>43.752758</td>
      <td>-79.400049</td>
    </tr>
    <tr>
      <td>24</td>
      <td>M2R</td>
      <td>North York</td>
      <td>Willowdale West</td>
      <td>43.782736</td>
      <td>-79.442259</td>
    </tr>
    <tr>
      <td>25</td>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
      <td>43.753259</td>
      <td>-79.329656</td>
    </tr>
    <tr>
      <td>26</td>
      <td>M3B</td>
      <td>North York</td>
      <td>Don Mills North</td>
      <td>43.745906</td>
      <td>-79.352188</td>
    </tr>
    <tr>
      <td>27</td>
      <td>M3C</td>
      <td>North York</td>
      <td>Flemingdon Park, Don Mills South</td>
      <td>43.725900</td>
      <td>-79.340923</td>
    </tr>
    <tr>
      <td>28</td>
      <td>M3H</td>
      <td>North York</td>
      <td>Bathurst Manor, Downsview North, Wilson Heights</td>
      <td>43.754328</td>
      <td>-79.442259</td>
    </tr>
    <tr>
      <td>29</td>
      <td>M3J</td>
      <td>North York</td>
      <td>Northwood Park, York University</td>
      <td>43.767980</td>
      <td>-79.487262</td>
    </tr>
    <tr>
      <td>30</td>
      <td>M3K</td>
      <td>North York</td>
      <td>CFB Toronto, Downsview East</td>
      <td>43.737473</td>
      <td>-79.464763</td>
    </tr>
    <tr>
      <td>31</td>
      <td>M3L</td>
      <td>North York</td>
      <td>Downsview West</td>
      <td>43.739015</td>
      <td>-79.506944</td>
    </tr>
    <tr>
      <td>32</td>
      <td>M3M</td>
      <td>North York</td>
      <td>Downsview Central</td>
      <td>43.728496</td>
      <td>-79.495697</td>
    </tr>
    <tr>
      <td>33</td>
      <td>M3N</td>
      <td>North York</td>
      <td>Downsview Northwest</td>
      <td>43.761631</td>
      <td>-79.520999</td>
    </tr>
    <tr>
      <td>34</td>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
      <td>43.725882</td>
      <td>-79.315572</td>
    </tr>
    <tr>
      <td>35</td>
      <td>M4B</td>
      <td>East York</td>
      <td>Woodbine Gardens, Parkview Hill</td>
      <td>43.706397</td>
      <td>-79.309937</td>
    </tr>
    <tr>
      <td>36</td>
      <td>M4C</td>
      <td>East York</td>
      <td>Woodbine Heights</td>
      <td>43.695344</td>
      <td>-79.318389</td>
    </tr>
    <tr>
      <td>37</td>
      <td>M4E</td>
      <td>East Toronto</td>
      <td>The Beaches</td>
      <td>43.676357</td>
      <td>-79.293031</td>
    </tr>
    <tr>
      <td>38</td>
      <td>M4G</td>
      <td>East York</td>
      <td>Leaside</td>
      <td>43.709060</td>
      <td>-79.363452</td>
    </tr>
    <tr>
      <td>39</td>
      <td>M4H</td>
      <td>East York</td>
      <td>Thorncliffe Park</td>
      <td>43.705369</td>
      <td>-79.349372</td>
    </tr>
    <tr>
      <td>40</td>
      <td>M4J</td>
      <td>East York</td>
      <td>East Toronto</td>
      <td>43.685347</td>
      <td>-79.338106</td>
    </tr>
    <tr>
      <td>41</td>
      <td>M4K</td>
      <td>East Toronto</td>
      <td>The Danforth West, Riverdale</td>
      <td>43.679557</td>
      <td>-79.352188</td>
    </tr>
    <tr>
      <td>42</td>
      <td>M4L</td>
      <td>East Toronto</td>
      <td>The Beaches West, India Bazaar</td>
      <td>43.668999</td>
      <td>-79.315572</td>
    </tr>
    <tr>
      <td>43</td>
      <td>M4M</td>
      <td>East Toronto</td>
      <td>Studio District</td>
      <td>43.659526</td>
      <td>-79.340923</td>
    </tr>
    <tr>
      <td>44</td>
      <td>M4N</td>
      <td>Central Toronto</td>
      <td>Lawrence Park</td>
      <td>43.728020</td>
      <td>-79.388790</td>
    </tr>
    <tr>
      <td>45</td>
      <td>M4P</td>
      <td>Central Toronto</td>
      <td>Davisville North</td>
      <td>43.712751</td>
      <td>-79.390197</td>
    </tr>
    <tr>
      <td>46</td>
      <td>M4R</td>
      <td>Central Toronto</td>
      <td>North Toronto West</td>
      <td>43.715383</td>
      <td>-79.405678</td>
    </tr>
    <tr>
      <td>47</td>
      <td>M4S</td>
      <td>Central Toronto</td>
      <td>Davisville</td>
      <td>43.704324</td>
      <td>-79.388790</td>
    </tr>
    <tr>
      <td>48</td>
      <td>M4T</td>
      <td>Central Toronto</td>
      <td>Moore Park, Summerhill East</td>
      <td>43.689574</td>
      <td>-79.383160</td>
    </tr>
    <tr>
      <td>49</td>
      <td>M4V</td>
      <td>Central Toronto</td>
      <td>Deer Park, Forest Hill SE, Rathnelly, South Hi...</td>
      <td>43.686412</td>
      <td>-79.400049</td>
    </tr>
    <tr>
      <td>50</td>
      <td>M4W</td>
      <td>Downtown Toronto</td>
      <td>Rosedale</td>
      <td>43.679563</td>
      <td>-79.377529</td>
    </tr>
    <tr>
      <td>51</td>
      <td>M4X</td>
      <td>Downtown Toronto</td>
      <td>Cabbagetown, St. James Town</td>
      <td>43.667967</td>
      <td>-79.367675</td>
    </tr>
    <tr>
      <td>52</td>
      <td>M4Y</td>
      <td>Downtown Toronto</td>
      <td>Church and Wellesley</td>
      <td>43.665860</td>
      <td>-79.383160</td>
    </tr>
    <tr>
      <td>53</td>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront</td>
      <td>43.654260</td>
      <td>-79.360636</td>
    </tr>
    <tr>
      <td>54</td>
      <td>M5B</td>
      <td>Downtown Toronto</td>
      <td>Ryerson, Garden District</td>
      <td>43.657162</td>
      <td>-79.378937</td>
    </tr>
    <tr>
      <td>55</td>
      <td>M5C</td>
      <td>Downtown Toronto</td>
      <td>St. James Town</td>
      <td>43.651494</td>
      <td>-79.375418</td>
    </tr>
    <tr>
      <td>56</td>
      <td>M5E</td>
      <td>Downtown Toronto</td>
      <td>Berczy Park</td>
      <td>43.644771</td>
      <td>-79.373306</td>
    </tr>
    <tr>
      <td>57</td>
      <td>M5G</td>
      <td>Downtown Toronto</td>
      <td>Central Bay Street</td>
      <td>43.657952</td>
      <td>-79.387383</td>
    </tr>
    <tr>
      <td>58</td>
      <td>M5H</td>
      <td>Downtown Toronto</td>
      <td>Adelaide, King, Richmond</td>
      <td>43.650571</td>
      <td>-79.384568</td>
    </tr>
    <tr>
      <td>59</td>
      <td>M5J</td>
      <td>Downtown Toronto</td>
      <td>Harbourfront East, Toronto Islands, Union Station</td>
      <td>43.640816</td>
      <td>-79.381752</td>
    </tr>
    <tr>
      <td>60</td>
      <td>M5K</td>
      <td>Downtown Toronto</td>
      <td>Design Exchange, Toronto Dominion Centre</td>
      <td>43.647177</td>
      <td>-79.381576</td>
    </tr>
    <tr>
      <td>61</td>
      <td>M5L</td>
      <td>Downtown Toronto</td>
      <td>Commerce Court, Victoria Hotel</td>
      <td>43.648198</td>
      <td>-79.379817</td>
    </tr>
    <tr>
      <td>62</td>
      <td>M5M</td>
      <td>North York</td>
      <td>Bedford Park, Lawrence Manor East</td>
      <td>43.733283</td>
      <td>-79.419750</td>
    </tr>
    <tr>
      <td>63</td>
      <td>M5N</td>
      <td>Central Toronto</td>
      <td>Roselawn</td>
      <td>43.711695</td>
      <td>-79.416936</td>
    </tr>
    <tr>
      <td>64</td>
      <td>M5P</td>
      <td>Central Toronto</td>
      <td>Forest Hill North, Forest Hill West</td>
      <td>43.696948</td>
      <td>-79.411307</td>
    </tr>
    <tr>
      <td>65</td>
      <td>M5R</td>
      <td>Central Toronto</td>
      <td>The Annex, North Midtown, Yorkville</td>
      <td>43.672710</td>
      <td>-79.405678</td>
    </tr>
    <tr>
      <td>66</td>
      <td>M5S</td>
      <td>Downtown Toronto</td>
      <td>Harbord, University of Toronto</td>
      <td>43.662696</td>
      <td>-79.400049</td>
    </tr>
    <tr>
      <td>67</td>
      <td>M5T</td>
      <td>Downtown Toronto</td>
      <td>Chinatown, Grange Park, Kensington Market</td>
      <td>43.653206</td>
      <td>-79.400049</td>
    </tr>
    <tr>
      <td>68</td>
      <td>M5V</td>
      <td>Downtown Toronto</td>
      <td>CN Tower, Bathurst Quay, Island airport, Harbo...</td>
      <td>43.628947</td>
      <td>-79.394420</td>
    </tr>
    <tr>
      <td>69</td>
      <td>M5W</td>
      <td>Downtown Toronto</td>
      <td>Stn A PO Boxes 25 The Esplanade</td>
      <td>43.646435</td>
      <td>-79.374846</td>
    </tr>
    <tr>
      <td>70</td>
      <td>M5X</td>
      <td>Downtown Toronto</td>
      <td>First Canadian Place, Underground city</td>
      <td>43.648429</td>
      <td>-79.382280</td>
    </tr>
    <tr>
      <td>71</td>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Heights, Lawrence Manor</td>
      <td>43.718518</td>
      <td>-79.464763</td>
    </tr>
    <tr>
      <td>72</td>
      <td>M6B</td>
      <td>North York</td>
      <td>Glencairn</td>
      <td>43.709577</td>
      <td>-79.445073</td>
    </tr>
    <tr>
      <td>73</td>
      <td>M6C</td>
      <td>York</td>
      <td>Humewood-Cedarvale</td>
      <td>43.693781</td>
      <td>-79.428191</td>
    </tr>
    <tr>
      <td>74</td>
      <td>M6E</td>
      <td>York</td>
      <td>Caledonia-Fairbanks</td>
      <td>43.689026</td>
      <td>-79.453512</td>
    </tr>
    <tr>
      <td>75</td>
      <td>M6G</td>
      <td>Downtown Toronto</td>
      <td>Christie</td>
      <td>43.669542</td>
      <td>-79.422564</td>
    </tr>
    <tr>
      <td>76</td>
      <td>M6H</td>
      <td>West Toronto</td>
      <td>Dovercourt Village, Dufferin</td>
      <td>43.669005</td>
      <td>-79.442259</td>
    </tr>
    <tr>
      <td>77</td>
      <td>M6J</td>
      <td>West Toronto</td>
      <td>Little Portugal, Trinity</td>
      <td>43.647927</td>
      <td>-79.419750</td>
    </tr>
    <tr>
      <td>78</td>
      <td>M6K</td>
      <td>West Toronto</td>
      <td>Brockton, Exhibition Place, Parkdale Village</td>
      <td>43.636847</td>
      <td>-79.428191</td>
    </tr>
    <tr>
      <td>79</td>
      <td>M6L</td>
      <td>North York</td>
      <td>Downsview, North Park, Upwood Park</td>
      <td>43.713756</td>
      <td>-79.490074</td>
    </tr>
    <tr>
      <td>80</td>
      <td>M6M</td>
      <td>York</td>
      <td>Del Ray, Keelesdale, Mount Dennis, Silverthorn</td>
      <td>43.691116</td>
      <td>-79.476013</td>
    </tr>
    <tr>
      <td>81</td>
      <td>M6N</td>
      <td>York</td>
      <td>The Junction North, Runnymede</td>
      <td>43.673185</td>
      <td>-79.487262</td>
    </tr>
    <tr>
      <td>82</td>
      <td>M6P</td>
      <td>West Toronto</td>
      <td>High Park, The Junction South</td>
      <td>43.661608</td>
      <td>-79.464763</td>
    </tr>
    <tr>
      <td>83</td>
      <td>M6R</td>
      <td>West Toronto</td>
      <td>Parkdale, Roncesvalles</td>
      <td>43.648960</td>
      <td>-79.456325</td>
    </tr>
    <tr>
      <td>84</td>
      <td>M6S</td>
      <td>West Toronto</td>
      <td>Runnymede, Swansea</td>
      <td>43.651571</td>
      <td>-79.484450</td>
    </tr>
    <tr>
      <td>85</td>
      <td>M7A</td>
      <td>Queen's Park</td>
      <td>Queen's Park</td>
      <td>43.662301</td>
      <td>-79.389494</td>
    </tr>
    <tr>
      <td>86</td>
      <td>M7R</td>
      <td>Mississauga</td>
      <td>Canada Post Gateway Processing Centre</td>
      <td>43.636966</td>
      <td>-79.615819</td>
    </tr>
    <tr>
      <td>87</td>
      <td>M7Y</td>
      <td>East Toronto</td>
      <td>Business Reply Mail Processing Centre 969 Eastern</td>
      <td>43.662744</td>
      <td>-79.321558</td>
    </tr>
    <tr>
      <td>88</td>
      <td>M8V</td>
      <td>Etobicoke</td>
      <td>Humber Bay Shores, Mimico South, New Toronto</td>
      <td>43.605647</td>
      <td>-79.501321</td>
    </tr>
    <tr>
      <td>89</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood, Long Branch</td>
      <td>43.602414</td>
      <td>-79.543484</td>
    </tr>
    <tr>
      <td>90</td>
      <td>M8X</td>
      <td>Etobicoke</td>
      <td>The Kingsway, Montgomery Road, Old Mill North</td>
      <td>43.653654</td>
      <td>-79.506944</td>
    </tr>
    <tr>
      <td>91</td>
      <td>M8Y</td>
      <td>Etobicoke</td>
      <td>Humber Bay, King's Mill Park, Kingsway Park So...</td>
      <td>43.636258</td>
      <td>-79.498509</td>
    </tr>
    <tr>
      <td>92</td>
      <td>M8Z</td>
      <td>Etobicoke</td>
      <td>Kingsway Park South West, Mimico NW, The Queen...</td>
      <td>43.628841</td>
      <td>-79.520999</td>
    </tr>
    <tr>
      <td>93</td>
      <td>M9A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park</td>
      <td>43.667856</td>
      <td>-79.532242</td>
    </tr>
    <tr>
      <td>94</td>
      <td>M9B</td>
      <td>Etobicoke</td>
      <td>Cloverdale, Islington, Martin Grove, Princess ...</td>
      <td>43.650943</td>
      <td>-79.554724</td>
    </tr>
    <tr>
      <td>95</td>
      <td>M9C</td>
      <td>Etobicoke</td>
      <td>Bloordale Gardens, Eringate, Markland Wood, Ol...</td>
      <td>43.643515</td>
      <td>-79.577201</td>
    </tr>
    <tr>
      <td>96</td>
      <td>M9L</td>
      <td>North York</td>
      <td>Humber Summit</td>
      <td>43.756303</td>
      <td>-79.565963</td>
    </tr>
    <tr>
      <td>97</td>
      <td>M9M</td>
      <td>North York</td>
      <td>Emery, Humberlea</td>
      <td>43.724766</td>
      <td>-79.532242</td>
    </tr>
    <tr>
      <td>98</td>
      <td>M9N</td>
      <td>York</td>
      <td>Weston</td>
      <td>43.706876</td>
      <td>-79.518188</td>
    </tr>
    <tr>
      <td>99</td>
      <td>M9P</td>
      <td>Etobicoke</td>
      <td>Westmount</td>
      <td>43.696319</td>
      <td>-79.532242</td>
    </tr>
    <tr>
      <td>100</td>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Kingsview Village, Martin Grove Gardens, Richv...</td>
      <td>43.688905</td>
      <td>-79.554724</td>
    </tr>
    <tr>
      <td>101</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens, Beaumond Heights, Humbergate, ...</td>
      <td>43.739416</td>
      <td>-79.588437</td>
    </tr>
    <tr>
      <td>102</td>
      <td>M9W</td>
      <td>Etobicoke</td>
      <td>Northwest</td>
      <td>43.706748</td>
      <td>-79.594054</td>
    </tr>
  </tbody>
</table>
</div>



## Code

#### First download all the dependencies that we will need


```python
import numpy as np # library to handle data in a vectorized manner

import pandas as pd # library for data analsysis
pd.set_option('display.max_columns', None)
pd.set_option('display.max_rows', None)

import json # library to handle JSON files

#!conda install -c conda-forge geopy --yes # uncomment this line if you haven't completed the Foursquare API lab
!conda install -c conda-forge geopy --yes 
from geopy.geocoders import Nominatim # convert an address into latitude and longitude values

import requests # library to handle requests
from pandas.io.json import json_normalize # tranform JSON file into a pandas dataframe

# Matplotlib and associated plotting modules
import matplotlib.cm as cm
import matplotlib.colors as colors

# import k-means from clustering stage
from sklearn.cluster import KMeans

#!conda install -c conda-forge folium=0.5.0 --yes # uncomment this line if you haven't completed the Foursquare API lab
!conda install -c conda-forge folium=0.5.0 --yes
import folium # map rendering library

print('Libraries imported.')
```

    Collecting package metadata (current_repodata.json): ...working... done
    Solving environment: ...working... done
    
    ## Package Plan ##
    
      environment location: C:\Users\saifu\Anaconda3
    
      added / updated specs:
        - geopy
    
    
    The following packages will be downloaded:
    
        package                    |            build
        ---------------------------|-----------------
        geographiclib-1.50         |             py_0          34 KB  conda-forge
        geopy-1.20.0               |             py_0          57 KB  conda-forge
        ------------------------------------------------------------
                                               Total:          91 KB
    
    The following NEW packages will be INSTALLED:
    
      geographiclib      conda-forge/noarch::geographiclib-1.50-py_0
      geopy              conda-forge/noarch::geopy-1.20.0-py_0
    
    
    
    Downloading and Extracting Packages
    
    geopy-1.20.0         | 57 KB     |            |   0% 
    geopy-1.20.0         | 57 KB     | ##7        |  28% 
    geopy-1.20.0         | 57 KB     | ########## | 100% 
    
    geographiclib-1.50   | 34 KB     |            |   0% 
    geographiclib-1.50   | 34 KB     | ########## | 100% 
    Preparing transaction: ...working... done
    Verifying transaction: ...working... done
    Executing transaction: ...working... done
    Collecting package metadata (current_repodata.json): ...working... done
    Solving environment: ...working... done
    
    # All requested packages already installed.
    
    Libraries imported.
    

#### Use "geopy" library to get the latitude and longitude values of **Toronto**


```python
address = 'Toronto City Center, CA'

geolocator = Nominatim(user_agent="ny_explorer")
location = geolocator.geocode(address)
latitude = location.latitude
longitude = location.longitude
print('The geograpical coordinate of Toronto City Center are {}, {}.'.format(latitude, longitude))
```

    The geograpical coordinate of Toronto City Center are 43.653963, -79.387207.
    

#### Create a map of Toronto with neighborhoods superimposed on top.


```python
# create map of Toronto using latitude and longitude values
map_Toronto = folium.Map(location=[latitude, longitude], zoom_start=10)

# add markers to map
for lat, lng, borough, neighborhood in zip(DataFrame['Latitude'], DataFrame['Longitude'], DataFrame['Borough'], DataFrame['Neighbourhood']):
    label = '{}, {}'.format(neighborhood, borough)
    label = folium.Popup(label, parse_html=True)
    folium.CircleMarker(
        [lat, lng],
        radius=5,
        popup=label,
        color='blue',
        fill=True,
        fill_color='#3186cc',
        fill_opacity=0.7,
        parse_html=False).add_to(map_Toronto)  
    
map_Toronto
```




<div style="width:100%;"><div style="position:relative;width:100%;height:0;padding-bottom:60%;"><iframe src="data:text/html;charset=utf-8;base64,PCFET0NUWVBFIGh0bWw+CjxoZWFkPiAgICAKICAgIDxtZXRhIGh0dHAtZXF1aXY9ImNvbnRlbnQtdHlwZSIgY29udGVudD0idGV4dC9odG1sOyBjaGFyc2V0PVVURi04IiAvPgogICAgPHNjcmlwdD5MX1BSRUZFUl9DQU5WQVMgPSBmYWxzZTsgTF9OT19UT1VDSCA9IGZhbHNlOyBMX0RJU0FCTEVfM0QgPSBmYWxzZTs8L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL2Nkbi5qc2RlbGl2ci5uZXQvbnBtL2xlYWZsZXRAMS4yLjAvZGlzdC9sZWFmbGV0LmpzIj48L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL2FqYXguZ29vZ2xlYXBpcy5jb20vYWpheC9saWJzL2pxdWVyeS8xLjExLjEvanF1ZXJ5Lm1pbi5qcyI+PC9zY3JpcHQ+CiAgICA8c2NyaXB0IHNyYz0iaHR0cHM6Ly9tYXhjZG4uYm9vdHN0cmFwY2RuLmNvbS9ib290c3RyYXAvMy4yLjAvanMvYm9vdHN0cmFwLm1pbi5qcyI+PC9zY3JpcHQ+CiAgICA8c2NyaXB0IHNyYz0iaHR0cHM6Ly9jZG5qcy5jbG91ZGZsYXJlLmNvbS9hamF4L2xpYnMvTGVhZmxldC5hd2Vzb21lLW1hcmtlcnMvMi4wLjIvbGVhZmxldC5hd2Vzb21lLW1hcmtlcnMuanMiPjwvc2NyaXB0PgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL2Nkbi5qc2RlbGl2ci5uZXQvbnBtL2xlYWZsZXRAMS4yLjAvZGlzdC9sZWFmbGV0LmNzcyIvPgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL21heGNkbi5ib290c3RyYXBjZG4uY29tL2Jvb3RzdHJhcC8zLjIuMC9jc3MvYm9vdHN0cmFwLm1pbi5jc3MiLz4KICAgIDxsaW5rIHJlbD0ic3R5bGVzaGVldCIgaHJlZj0iaHR0cHM6Ly9tYXhjZG4uYm9vdHN0cmFwY2RuLmNvbS9ib290c3RyYXAvMy4yLjAvY3NzL2Jvb3RzdHJhcC10aGVtZS5taW4uY3NzIi8+CiAgICA8bGluayByZWw9InN0eWxlc2hlZXQiIGhyZWY9Imh0dHBzOi8vbWF4Y2RuLmJvb3RzdHJhcGNkbi5jb20vZm9udC1hd2Vzb21lLzQuNi4zL2Nzcy9mb250LWF3ZXNvbWUubWluLmNzcyIvPgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL2NkbmpzLmNsb3VkZmxhcmUuY29tL2FqYXgvbGlicy9MZWFmbGV0LmF3ZXNvbWUtbWFya2Vycy8yLjAuMi9sZWFmbGV0LmF3ZXNvbWUtbWFya2Vycy5jc3MiLz4KICAgIDxsaW5rIHJlbD0ic3R5bGVzaGVldCIgaHJlZj0iaHR0cHM6Ly9yYXdnaXQuY29tL3B5dGhvbi12aXN1YWxpemF0aW9uL2ZvbGl1bS9tYXN0ZXIvZm9saXVtL3RlbXBsYXRlcy9sZWFmbGV0LmF3ZXNvbWUucm90YXRlLmNzcyIvPgogICAgPHN0eWxlPmh0bWwsIGJvZHkge3dpZHRoOiAxMDAlO2hlaWdodDogMTAwJTttYXJnaW46IDA7cGFkZGluZzogMDt9PC9zdHlsZT4KICAgIDxzdHlsZT4jbWFwIHtwb3NpdGlvbjphYnNvbHV0ZTt0b3A6MDtib3R0b206MDtyaWdodDowO2xlZnQ6MDt9PC9zdHlsZT4KICAgIAogICAgICAgICAgICA8c3R5bGU+ICNtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMgewogICAgICAgICAgICAgICAgcG9zaXRpb24gOiByZWxhdGl2ZTsKICAgICAgICAgICAgICAgIHdpZHRoIDogMTAwLjAlOwogICAgICAgICAgICAgICAgaGVpZ2h0OiAxMDAuMCU7CiAgICAgICAgICAgICAgICBsZWZ0OiAwLjAlOwogICAgICAgICAgICAgICAgdG9wOiAwLjAlOwogICAgICAgICAgICAgICAgfQogICAgICAgICAgICA8L3N0eWxlPgogICAgICAgIAo8L2hlYWQ+Cjxib2R5PiAgICAKICAgIAogICAgICAgICAgICA8ZGl2IGNsYXNzPSJmb2xpdW0tbWFwIiBpZD0ibWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzIiA+PC9kaXY+CiAgICAgICAgCjwvYm9keT4KPHNjcmlwdD4gICAgCiAgICAKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGJvdW5kcyA9IG51bGw7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgdmFyIG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyA9IEwubWFwKAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgJ21hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMycsCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICB7Y2VudGVyOiBbNDMuNjUzOTYzLC03OS4zODcyMDddLAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgem9vbTogMTAsCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICBtYXhCb3VuZHM6IGJvdW5kcywKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIGxheWVyczogW10sCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICB3b3JsZENvcHlKdW1wOiBmYWxzZSwKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIGNyczogTC5DUlMuRVBTRzM4NTcKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgfSk7CiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciB0aWxlX2xheWVyX2E5Y2MyNmE1YWFmZjRiYzdiZmY1M2U4ZmY4NzQ2ZGQ2ID0gTC50aWxlTGF5ZXIoCiAgICAgICAgICAgICAgICAnaHR0cHM6Ly97c30udGlsZS5vcGVuc3RyZWV0bWFwLm9yZy97en0ve3h9L3t5fS5wbmcnLAogICAgICAgICAgICAgICAgewogICJhdHRyaWJ1dGlvbiI6IG51bGwsCiAgImRldGVjdFJldGluYSI6IGZhbHNlLAogICJtYXhab29tIjogMTgsCiAgIm1pblpvb20iOiAxLAogICJub1dyYXAiOiBmYWxzZSwKICAic3ViZG9tYWlucyI6ICJhYmMiCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl82MmQ5M2Y1YWQ1MGI0ZDA4YjhkZWE4OTI4MTNmMWQxNCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjgwNjY4NjI5OTk5OTk5NiwtNzkuMTk0MzUzNDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMjFmNDY4YTZhN2I1NDdlZTg2YjgzZjFiZmI0OWQyZmUgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMmJhMDQ2NjU0NjJhNDkxMzliZmFjYmNlOWQ3OWU0ZDEgPSAkKCc8ZGl2IGlkPSJodG1sXzJiYTA0NjY1NDYyYTQ5MTM5YmZhY2JjZTlkNzllNGQxIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Sb3VnZSwgTWFsdmVybiwgU2NhcmJvcm91Z2g8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzIxZjQ2OGE2YTdiNTQ3ZWU4NmI4M2YxYmZiNDlkMmZlLnNldENvbnRlbnQoaHRtbF8yYmEwNDY2NTQ2MmE0OTEzOWJmYWNiY2U5ZDc5ZTRkMSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl82MmQ5M2Y1YWQ1MGI0ZDA4YjhkZWE4OTI4MTNmMWQxNC5iaW5kUG9wdXAocG9wdXBfMjFmNDY4YTZhN2I1NDdlZTg2YjgzZjFiZmI0OWQyZmUpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfZWNhMTE5ZTBmNmEyNDgzOWI1OWI2NjQwZThkZjFkNjggPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43ODQ1MzUxLC03OS4xNjA0OTcwOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF83MGRjMWFiMTg4M2Y0ZmEyYTlkMTBlZWRhNDkxMTdkMyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9iM2MzMTI5OWY0OTM0MDljOTY0YThiNjVhYmUwNzRlYyA9ICQoJzxkaXYgaWQ9Imh0bWxfYjNjMzEyOTlmNDkzNDA5Yzk2NGE4YjY1YWJlMDc0ZWMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkhpZ2hsYW5kIENyZWVrLCBSb3VnZSBIaWxsLCBQb3J0IFVuaW9uLCBTY2FyYm9yb3VnaDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNzBkYzFhYjE4ODNmNGZhMmE5ZDEwZWVkYTQ5MTE3ZDMuc2V0Q29udGVudChodG1sX2IzYzMxMjk5ZjQ5MzQwOWM5NjRhOGI2NWFiZTA3NGVjKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2VjYTExOWUwZjZhMjQ4MzliNTliNjY0MGU4ZGYxZDY4LmJpbmRQb3B1cChwb3B1cF83MGRjMWFiMTg4M2Y0ZmEyYTlkMTBlZWRhNDkxMTdkMyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl84ZDQ4Y2NiNTc1MDg0ZGY2YTBiMzVlZWZkOTY5ODQwZiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc2MzU3MjYsLTc5LjE4ODcxMTVdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfN2ZkN2Q4NjZiYWI2NDc0MmE0NTYwNDEzNGQ5MWNiZmUgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfY2I5ZDBhMTY2Y2FjNDI2ZmI4MjMyMTAxMTc1MDg2OGMgPSAkKCc8ZGl2IGlkPSJodG1sX2NiOWQwYTE2NmNhYzQyNmZiODIzMjEwMTE3NTA4NjhjIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5HdWlsZHdvb2QsIE1vcm5pbmdzaWRlLCBXZXN0IEhpbGwsIFNjYXJib3JvdWdoPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF83ZmQ3ZDg2NmJhYjY0NzQyYTQ1NjA0MTM0ZDkxY2JmZS5zZXRDb250ZW50KGh0bWxfY2I5ZDBhMTY2Y2FjNDI2ZmI4MjMyMTAxMTc1MDg2OGMpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfOGQ0OGNjYjU3NTA4NGRmNmEwYjM1ZWVmZDk2OTg0MGYuYmluZFBvcHVwKHBvcHVwXzdmZDdkODY2YmFiNjQ3NDJhNDU2MDQxMzRkOTFjYmZlKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2QwODc2NTg5YzQ2MzQ0NzU5ODI2MGRlNmQ1MDMyMzAzID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzcwOTkyMSwtNzkuMjE2OTE3NDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfZDIyMDYzNGRhMTBiNDE2NDhjYzliMGM2OTg1YWQ2OGUgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMWEyODQwMDQ1MzBjNDhhOWI1N2E2NmUzOGI5YTYyYjggPSAkKCc8ZGl2IGlkPSJodG1sXzFhMjg0MDA0NTMwYzQ4YTliNTdhNjZlMzhiOWE2MmI4IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Xb2J1cm4sIFNjYXJib3JvdWdoPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9kMjIwNjM0ZGExMGI0MTY0OGNjOWIwYzY5ODVhZDY4ZS5zZXRDb250ZW50KGh0bWxfMWEyODQwMDQ1MzBjNDhhOWI1N2E2NmUzOGI5YTYyYjgpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfZDA4NzY1ODljNDYzNDQ3NTk4MjYwZGU2ZDUwMzIzMDMuYmluZFBvcHVwKHBvcHVwX2QyMjA2MzRkYTEwYjQxNjQ4Y2M5YjBjNjk4NWFkNjhlKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzJiZDRmYzBlOGYzZDQ1OWNhMjFhODcwNTE1MjBjODczID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzczMTM2LC03OS4yMzk0NzYwOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9lYWJhMjk5NmY0MWY0ZWFjYThiMDQzMDgzNTIyMDA0NCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF82ZjAwYjIwYThhOGQ0YjEwODZmNDc5YzJkN2NhM2RkNyA9ICQoJzxkaXYgaWQ9Imh0bWxfNmYwMGIyMGE4YThkNGIxMDg2ZjQ3OWMyZDdjYTNkZDciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNlZGFyYnJhZSwgU2NhcmJvcm91Z2g8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2VhYmEyOTk2ZjQxZjRlYWNhOGIwNDMwODM1MjIwMDQ0LnNldENvbnRlbnQoaHRtbF82ZjAwYjIwYThhOGQ0YjEwODZmNDc5YzJkN2NhM2RkNyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8yYmQ0ZmMwZThmM2Q0NTljYTIxYTg3MDUxNTIwYzg3My5iaW5kUG9wdXAocG9wdXBfZWFiYTI5OTZmNDFmNGVhY2E4YjA0MzA4MzUyMjAwNDQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMDdiYzg2Zjk4OTM4NGQwMDkwNzBmYjFlMjM3ZDQ4ZDggPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43NDQ3MzQyLC03OS4yMzk0NzYwOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9hNzIzMmQwMDg0YjM0OGRlYmU3MWY5MTJjNjUxN2U5YyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9jYTIxZDhiYTI2MmU0OWM5OTQ0OWVjYTdmM2VhNDE4OCA9ICQoJzxkaXYgaWQ9Imh0bWxfY2EyMWQ4YmEyNjJlNDljOTk0NDllY2E3ZjNlYTQxODgiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlNjYXJib3JvdWdoIFZpbGxhZ2UsIFNjYXJib3JvdWdoPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9hNzIzMmQwMDg0YjM0OGRlYmU3MWY5MTJjNjUxN2U5Yy5zZXRDb250ZW50KGh0bWxfY2EyMWQ4YmEyNjJlNDljOTk0NDllY2E3ZjNlYTQxODgpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMDdiYzg2Zjk4OTM4NGQwMDkwNzBmYjFlMjM3ZDQ4ZDguYmluZFBvcHVwKHBvcHVwX2E3MjMyZDAwODRiMzQ4ZGViZTcxZjkxMmM2NTE3ZTljKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2VlMDI4YzM2NTk4MDQ2MDBhMTJkOGQzOWQ4YWM5MzNlID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzI3OTI5MiwtNzkuMjYyMDI5NDAwMDAwMDJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfOTc5MTZmZmY2MzhlNGM5OWJkZGE2MGRiNzM5YjMxMzIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfZTFhNTdkYTZmMDU0NDZlMWE1MGQzNTk0YTQxMTc4ZDYgPSAkKCc8ZGl2IGlkPSJodG1sX2UxYTU3ZGE2ZjA1NDQ2ZTFhNTBkMzU5NGE0MTE3OGQ2IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5FYXN0IEJpcmNobW91bnQgUGFyaywgSW9udmlldywgS2VubmVkeSBQYXJrLCBTY2FyYm9yb3VnaDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfOTc5MTZmZmY2MzhlNGM5OWJkZGE2MGRiNzM5YjMxMzIuc2V0Q29udGVudChodG1sX2UxYTU3ZGE2ZjA1NDQ2ZTFhNTBkMzU5NGE0MTE3OGQ2KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2VlMDI4YzM2NTk4MDQ2MDBhMTJkOGQzOWQ4YWM5MzNlLmJpbmRQb3B1cChwb3B1cF85NzkxNmZmZjYzOGU0Yzk5YmRkYTYwZGI3MzliMzEzMik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8yYThkMzg1NGE4NTY0YzUxYmI4ZDIwOGZlYzY4NWI1YiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcxMTExMTcwMDAwMDAwNCwtNzkuMjg0NTc3Ml0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9iYjYwZGNhZDdhMGM0NzBmOWQzMzUwODRjNTAyM2JjMSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9mZDljMDNjMDJkMzA0ZjYxYjFlZDkwOWRlNWE4MWUyNyA9ICQoJzxkaXYgaWQ9Imh0bWxfZmQ5YzAzYzAyZDMwNGY2MWIxZWQ5MDlkZTVhODFlMjciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNsYWlybGVhLCBHb2xkZW4gTWlsZSwgT2FrcmlkZ2UsIFNjYXJib3JvdWdoPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9iYjYwZGNhZDdhMGM0NzBmOWQzMzUwODRjNTAyM2JjMS5zZXRDb250ZW50KGh0bWxfZmQ5YzAzYzAyZDMwNGY2MWIxZWQ5MDlkZTVhODFlMjcpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMmE4ZDM4NTRhODU2NGM1MWJiOGQyMDhmZWM2ODViNWIuYmluZFBvcHVwKHBvcHVwX2JiNjBkY2FkN2EwYzQ3MGY5ZDMzNTA4NGM1MDIzYmMxKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzNmOTNiMDA4YTM1OTRhMjJiOWRmYjhlOTJhYTliOGY1ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzE2MzE2LC03OS4yMzk0NzYwOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9mOTU4YTM3ZDc5M2Q0ZjExYjdlOGU2N2VhZWJjMWVkYiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF85NWZjMjRkN2M1MjI0MWRkYjNhMDFiM2I4YzE5ZjIzNiA9ICQoJzxkaXYgaWQ9Imh0bWxfOTVmYzI0ZDdjNTIyNDFkZGIzYTAxYjNiOGMxOWYyMzYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNsaWZmY3Jlc3QsIENsaWZmc2lkZSwgU2NhcmJvcm91Z2ggVmlsbGFnZSBXZXN0LCBTY2FyYm9yb3VnaDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZjk1OGEzN2Q3OTNkNGYxMWI3ZThlNjdlYWViYzFlZGIuc2V0Q29udGVudChodG1sXzk1ZmMyNGQ3YzUyMjQxZGRiM2EwMWIzYjhjMTlmMjM2KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzNmOTNiMDA4YTM1OTRhMjJiOWRmYjhlOTJhYTliOGY1LmJpbmRQb3B1cChwb3B1cF9mOTU4YTM3ZDc5M2Q0ZjExYjdlOGU2N2VhZWJjMWVkYik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl84YzMxZDM4MDUyOTA0NGI5ODkxMmE1MzRhYzY5NWZlZSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY5MjY1NzAwMDAwMDAwNCwtNzkuMjY0ODQ4MV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8zNTIyNTJlNTU2OGE0YTI2YmE0YzQyY2ZiOWE1YmRmZSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9jZWYxNWYxMzAxNzc0NjBkYjZlNjcxMzk4OWVlY2Q5ZiA9ICQoJzxkaXYgaWQ9Imh0bWxfY2VmMTVmMTMwMTc3NDYwZGI2ZTY3MTM5ODllZWNkOWYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkJpcmNoIENsaWZmLCBDbGlmZnNpZGUgV2VzdCwgU2NhcmJvcm91Z2g8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzM1MjI1MmU1NTY4YTRhMjZiYTRjNDJjZmI5YTViZGZlLnNldENvbnRlbnQoaHRtbF9jZWYxNWYxMzAxNzc0NjBkYjZlNjcxMzk4OWVlY2Q5Zik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl84YzMxZDM4MDUyOTA0NGI5ODkxMmE1MzRhYzY5NWZlZS5iaW5kUG9wdXAocG9wdXBfMzUyMjUyZTU1NjhhNGEyNmJhNGM0MmNmYjlhNWJkZmUpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYmY0Mjc4ZjhhZjFlNGEzZGI0ZWIwNDJkOGE2Yjc5OTAgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43NTc0MDk2LC03OS4yNzMzMDQwMDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9hY2E0YWI0YWFlNTk0MThmOTAzNzIyZWNkMmU3YWFlMSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9mNDQ0ZGViNzI3MzE0Nzg2OGNiMzU0NmY2NDBmYmJiZCA9ICQoJzxkaXYgaWQ9Imh0bWxfZjQ0NGRlYjcyNzMxNDc4NjhjYjM1NDZmNjQwZmJiYmQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkRvcnNldCBQYXJrLCBTY2FyYm9yb3VnaCBUb3duIENlbnRyZSwgV2V4Zm9yZCBIZWlnaHRzLCBTY2FyYm9yb3VnaDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfYWNhNGFiNGFhZTU5NDE4ZjkwMzcyMmVjZDJlN2FhZTEuc2V0Q29udGVudChodG1sX2Y0NDRkZWI3MjczMTQ3ODY4Y2IzNTQ2ZjY0MGZiYmJkKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2JmNDI3OGY4YWYxZTRhM2RiNGViMDQyZDhhNmI3OTkwLmJpbmRQb3B1cChwb3B1cF9hY2E0YWI0YWFlNTk0MThmOTAzNzIyZWNkMmU3YWFlMSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9jZGYyNGU4ZTA2Njc0MGUzYmZhOTQzYjQxMTFmM2ZjOSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc1MDA3MTUwMDAwMDAwNCwtNzkuMjk1ODQ5MV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF83MjNiYjU3YmEzMTI0ZjkzYjAyZmFjNjNhNTAxNTA1YyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8zYmQ5MjFhMWNhNDI0NTQxOTZlNGZhMzk0NzI2YjFkZSA9ICQoJzxkaXYgaWQ9Imh0bWxfM2JkOTIxYTFjYTQyNDU0MTk2ZTRmYTM5NDcyNmIxZGUiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk1hcnl2YWxlLCBXZXhmb3JkLCBTY2FyYm9yb3VnaDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNzIzYmI1N2JhMzEyNGY5M2IwMmZhYzYzYTUwMTUwNWMuc2V0Q29udGVudChodG1sXzNiZDkyMWExY2E0MjQ1NDE5NmU0ZmEzOTQ3MjZiMWRlKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2NkZjI0ZThlMDY2NzQwZTNiZmE5NDNiNDExMWYzZmM5LmJpbmRQb3B1cChwb3B1cF83MjNiYjU3YmEzMTI0ZjkzYjAyZmFjNjNhNTAxNTA1Yyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl80MGIxMjc2NjMwOGQ0Njg5YWRhMTdhNjBkZjM1M2VkNCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc5NDIwMDMsLTc5LjI2MjAyOTQwMDAwMDAyXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzI0MWIwM2Q4ZDRiYjRiZGJhYTY4NDhlN2ViMTQ1YmRkID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2Q2ODRhZmQ5OTdiYzRhYjBhNDViZDYzZmE1OWY0NmJkID0gJCgnPGRpdiBpZD0iaHRtbF9kNjg0YWZkOTk3YmM0YWIwYTQ1YmQ2M2ZhNTlmNDZiZCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+QWdpbmNvdXJ0LCBTY2FyYm9yb3VnaDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMjQxYjAzZDhkNGJiNGJkYmFhNjg0OGU3ZWIxNDViZGQuc2V0Q29udGVudChodG1sX2Q2ODRhZmQ5OTdiYzRhYjBhNDViZDYzZmE1OWY0NmJkKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzQwYjEyNzY2MzA4ZDQ2ODlhZGExN2E2MGRmMzUzZWQ0LmJpbmRQb3B1cChwb3B1cF8yNDFiMDNkOGQ0YmI0YmRiYWE2ODQ4ZTdlYjE0NWJkZCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9mYTA2MzkzNjk0OGQ0M2M1OTYwNGVmMGZjOWYzMWViOSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc4MTYzNzUsLTc5LjMwNDMwMjFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfZGY1YzE5MTFiMGJiNDlmZThmZWRjYWRlYzg3YTQ4ZTcgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNTA3MWE0MzhiMjEzNDc0MDljZmY1YTQyZWI0MzZlYjMgPSAkKCc8ZGl2IGlkPSJodG1sXzUwNzFhNDM4YjIxMzQ3NDA5Y2ZmNWE0MmViNDM2ZWIzIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5DbGFya3MgQ29ybmVycywgU3VsbGl2YW4sIFRhbSBPJiMzOTtTaGFudGVyLCBTY2FyYm9yb3VnaDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZGY1YzE5MTFiMGJiNDlmZThmZWRjYWRlYzg3YTQ4ZTcuc2V0Q29udGVudChodG1sXzUwNzFhNDM4YjIxMzQ3NDA5Y2ZmNWE0MmViNDM2ZWIzKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2ZhMDYzOTM2OTQ4ZDQzYzU5NjA0ZWYwZmM5ZjMxZWI5LmJpbmRQb3B1cChwb3B1cF9kZjVjMTkxMWIwYmI0OWZlOGZlZGNhZGVjODdhNDhlNyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl80MThjYjliNGJlMTE0MDBjODlhOTc0YmNlNGY0NGM4ZCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjgxNTI1MjIsLTc5LjI4NDU3NzJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfOWJmNzY5YWIyYjdkNDRiYzgwNGVhODVkMWZkNTgxZTkgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfY2I5MzgwY2FjOTNhNDU2ZGE4ZGRjYmIyYTdkOWZjODkgPSAkKCc8ZGl2IGlkPSJodG1sX2NiOTM4MGNhYzkzYTQ1NmRhOGRkY2JiMmE3ZDlmYzg5IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5BZ2luY291cnQgTm9ydGgsIEwmIzM5O0Ftb3JlYXV4IEVhc3QsIE1pbGxpa2VuLCBTdGVlbGVzIEVhc3QsIFNjYXJib3JvdWdoPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF85YmY3NjlhYjJiN2Q0NGJjODA0ZWE4NWQxZmQ1ODFlOS5zZXRDb250ZW50KGh0bWxfY2I5MzgwY2FjOTNhNDU2ZGE4ZGRjYmIyYTdkOWZjODkpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNDE4Y2I5YjRiZTExNDAwYzg5YTk3NGJjZTRmNDRjOGQuYmluZFBvcHVwKHBvcHVwXzliZjc2OWFiMmI3ZDQ0YmM4MDRlYTg1ZDFmZDU4MWU5KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzM2YTY0MmU0MTMzZTQ5Mzk5OWY5NzcxMTI2OTQwYWRlID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzk5NTI1MjAwMDAwMDA1LC03OS4zMTgzODg3XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzBiMDg5MWQwM2FiNTQ1ZjZhNTg4YjI5NjE4NTZlNGE5ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzgzNzA4MDAwODE0ZjRiYzFiNmE3ZmQzOTljYzhiMjliID0gJCgnPGRpdiBpZD0iaHRtbF84MzcwODAwMDgxNGY0YmMxYjZhN2ZkMzk5Y2M4YjI5YiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TCYjMzk7QW1vcmVhdXggV2VzdCwgU2NhcmJvcm91Z2g8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzBiMDg5MWQwM2FiNTQ1ZjZhNTg4YjI5NjE4NTZlNGE5LnNldENvbnRlbnQoaHRtbF84MzcwODAwMDgxNGY0YmMxYjZhN2ZkMzk5Y2M4YjI5Yik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8zNmE2NDJlNDEzM2U0OTM5OTlmOTc3MTEyNjk0MGFkZS5iaW5kUG9wdXAocG9wdXBfMGIwODkxZDAzYWI1NDVmNmE1ODhiMjk2MTg1NmU0YTkpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOWM0ZDVmMzAzNjNlNDk2YWExZjI0YjVlOTFmOTJkM2MgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My44MzYxMjQ3MDAwMDAwMDYsLTc5LjIwNTYzNjA5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzI5YzlmMmI5MTNmODQ3YmFhOWQwYWIxODNmZjAwZTMxID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2E4ZjIzZGI1NjAwNDRkYjZhZDNiM2VlNjE2ZTExY2FkID0gJCgnPGRpdiBpZD0iaHRtbF9hOGYyM2RiNTYwMDQ0ZGI2YWQzYjNlZTYxNmUxMWNhZCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+VXBwZXIgUm91Z2UsIFNjYXJib3JvdWdoPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8yOWM5ZjJiOTEzZjg0N2JhYTlkMGFiMTgzZmYwMGUzMS5zZXRDb250ZW50KGh0bWxfYThmMjNkYjU2MDA0NGRiNmFkM2IzZWU2MTZlMTFjYWQpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfOWM0ZDVmMzAzNjNlNDk2YWExZjI0YjVlOTFmOTJkM2MuYmluZFBvcHVwKHBvcHVwXzI5YzlmMmI5MTNmODQ3YmFhOWQwYWIxODNmZjAwZTMxKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzJiMzI0NGI3ZDhlYzRlZDc4M2UwN2JkMzQxODBkMzRhID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuODAzNzYyMiwtNzkuMzYzNDUxN10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF84MjdkNGM0YzI2MWQ0ZTMzOTZlMWRlMjNkMTcyZTg2YSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9iMTc5NzQ5YjAyYzE0MzhlYjQyNDM3N2U1NzYwMjNmNSA9ICQoJzxkaXYgaWQ9Imh0bWxfYjE3OTc0OWIwMmMxNDM4ZWI0MjQzNzdlNTc2MDIzZjUiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkhpbGxjcmVzdCBWaWxsYWdlLCBOb3J0aCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF84MjdkNGM0YzI2MWQ0ZTMzOTZlMWRlMjNkMTcyZTg2YS5zZXRDb250ZW50KGh0bWxfYjE3OTc0OWIwMmMxNDM4ZWI0MjQzNzdlNTc2MDIzZjUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMmIzMjQ0YjdkOGVjNGVkNzgzZTA3YmQzNDE4MGQzNGEuYmluZFBvcHVwKHBvcHVwXzgyN2Q0YzRjMjYxZDRlMzM5NmUxZGUyM2QxNzJlODZhKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2NkYjllODlhOWY4MzQxNzY5NTg5N2E1MjNlOTcyODg4ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzc4NTE3NSwtNzkuMzQ2NTU1N10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8yMzEzZTZhZDRlOTk0MGIwYWUyZjVmMjA4NjdiYTRmMSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF80NzQ1MzM3MTcyYTg0YWUyYWI4MjhhZDIzODM3NDEyMSA9ICQoJzxkaXYgaWQ9Imh0bWxfNDc0NTMzNzE3MmE4NGFlMmFiODI4YWQyMzgzNzQxMjEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkZhaXJ2aWV3LCBIZW5yeSBGYXJtLCBPcmlvbGUsIE5vcnRoIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzIzMTNlNmFkNGU5OTQwYjBhZTJmNWYyMDg2N2JhNGYxLnNldENvbnRlbnQoaHRtbF80NzQ1MzM3MTcyYTg0YWUyYWI4MjhhZDIzODM3NDEyMSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9jZGI5ZTg5YTlmODM0MTc2OTU4OTdhNTIzZTk3Mjg4OC5iaW5kUG9wdXAocG9wdXBfMjMxM2U2YWQ0ZTk5NDBiMGFlMmY1ZjIwODY3YmE0ZjEpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYTBkMmQ0MzEwY2YwNGNiY2EzZWVhODU4M2NjOTM1NjMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43ODY5NDczLC03OS4zODU5NzVdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfOTE2ZWNjMzVjYzQyNGNmM2EwOTI1ODkxNTY2ZjU3OTggPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYWUwNzM2OGY1OGE3NDM5Y2FlN2VlNjUwZGNjYjY1NjYgPSAkKCc8ZGl2IGlkPSJodG1sX2FlMDczNjhmNThhNzQzOWNhZTdlZTY1MGRjY2I2NTY2IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5CYXl2aWV3IFZpbGxhZ2UsIE5vcnRoIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzkxNmVjYzM1Y2M0MjRjZjNhMDkyNTg5MTU2NmY1Nzk4LnNldENvbnRlbnQoaHRtbF9hZTA3MzY4ZjU4YTc0MzljYWU3ZWU2NTBkY2NiNjU2Nik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9hMGQyZDQzMTBjZjA0Y2JjYTNlZWE4NTgzY2M5MzU2My5iaW5kUG9wdXAocG9wdXBfOTE2ZWNjMzVjYzQyNGNmM2EwOTI1ODkxNTY2ZjU3OTgpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNjAxODc3MTdhMmFjNDkwZjk4OWMwYzQ3NWNmZmM1YzYgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43NTc0OTAyLC03OS4zNzQ3MTQwOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9jZjBjYzkyMzBkNmI0NGI0YjU5NDgyOTYyNjg0MjYyYiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF85NDlmMWZmYjAxZGQ0ZjdjOTJlNmFiODM0OTUzMzJlNCA9ICQoJzxkaXYgaWQ9Imh0bWxfOTQ5ZjFmZmIwMWRkNGY3YzkyZTZhYjgzNDk1MzMyZTQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlNpbHZlciBIaWxscywgWW9yayBNaWxscywgTm9ydGggWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfY2YwY2M5MjMwZDZiNDRiNGI1OTQ4Mjk2MjY4NDI2MmIuc2V0Q29udGVudChodG1sXzk0OWYxZmZiMDFkZDRmN2M5MmU2YWI4MzQ5NTMzMmU0KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzYwMTg3NzE3YTJhYzQ5MGY5ODljMGM0NzVjZmZjNWM2LmJpbmRQb3B1cChwb3B1cF9jZjBjYzkyMzBkNmI0NGI0YjU5NDgyOTYyNjg0MjYyYik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl84OGI3NTg1ODAyNDk0MGFiYTkyMjM2MjIxNjVmM2ZkOCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc4OTA1MywtNzkuNDA4NDkyNzk5OTk5OTldLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYzQwNGYxZWIzZjJjNDM2ZGFhNTU2Y2U4ZDFkZTMwMzUgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMWM3OTBmY2NmNTRmNGNjOGI0NTc3ZGJmMWZkZjBlMTEgPSAkKCc8ZGl2IGlkPSJodG1sXzFjNzkwZmNjZjU0ZjRjYzhiNDU3N2RiZjFmZGYwZTExIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5OZXd0b25icm9vaywgV2lsbG93ZGFsZSwgTm9ydGggWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfYzQwNGYxZWIzZjJjNDM2ZGFhNTU2Y2U4ZDFkZTMwMzUuc2V0Q29udGVudChodG1sXzFjNzkwZmNjZjU0ZjRjYzhiNDU3N2RiZjFmZGYwZTExKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzg4Yjc1ODU4MDI0OTQwYWJhOTIyMzYyMjE2NWYzZmQ4LmJpbmRQb3B1cChwb3B1cF9jNDA0ZjFlYjNmMmM0MzZkYWE1NTZjZThkMWRlMzAzNSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9kZjNiYjRmMWQ1NDk0OTM3OGJkNDFjMjY0MmM2NzZkYiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc3MDExOTksLTc5LjQwODQ5Mjc5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzQzN2EyNDdmM2MzNDRmODQ5ZjliMWFiNmYzNjk4ODQyID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzAxNWU0YzJhZGIxYTRlNGY4NWQ0NzlkZDRlZTE5MDQ3ID0gJCgnPGRpdiBpZD0iaHRtbF8wMTVlNGMyYWRiMWE0ZTRmODVkNDc5ZGQ0ZWUxOTA0NyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V2lsbG93ZGFsZSBTb3V0aCwgTm9ydGggWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNDM3YTI0N2YzYzM0NGY4NDlmOWIxYWI2ZjM2OTg4NDIuc2V0Q29udGVudChodG1sXzAxNWU0YzJhZGIxYTRlNGY4NWQ0NzlkZDRlZTE5MDQ3KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2RmM2JiNGYxZDU0OTQ5Mzc4YmQ0MWMyNjQyYzY3NmRiLmJpbmRQb3B1cChwb3B1cF80MzdhMjQ3ZjNjMzQ0Zjg0OWY5YjFhYjZmMzY5ODg0Mik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl85NThiOTU4M2ZjYTE0ODM1YjFlZDViY2Y3ZjcwMWZhZCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc1Mjc1ODI5OTk5OTk5NiwtNzkuNDAwMDQ5M10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF83NzhhYjczYTYzNjE0NjNjOWExNzFmNzQ4OGQ4OTYzOSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF81MGRmNDdiOTU0YzI0NjNjYTU1OTJhMjZiNWQwMTFmMiA9ICQoJzxkaXYgaWQ9Imh0bWxfNTBkZjQ3Yjk1NGMyNDYzY2E1NTkyYTI2YjVkMDExZjIiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPllvcmsgTWlsbHMgV2VzdCwgTm9ydGggWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNzc4YWI3M2E2MzYxNDYzYzlhMTcxZjc0ODhkODk2Mzkuc2V0Q29udGVudChodG1sXzUwZGY0N2I5NTRjMjQ2M2NhNTU5MmEyNmI1ZDAxMWYyKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzk1OGI5NTgzZmNhMTQ4MzViMWVkNWJjZjdmNzAxZmFkLmJpbmRQb3B1cChwb3B1cF83NzhhYjczYTYzNjE0NjNjOWExNzFmNzQ4OGQ4OTYzOSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9iOWZiYTEzNjc0NjY0YTllYTZjNmM2OTBlNjJiMmQ2OSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc4MjczNjQsLTc5LjQ0MjI1OTNdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfZTJiM2I5Y2Y0ODdiNGIyM2I4ZGVjZWJkMDc5NGY4N2IgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfY2Q2MDZkZjNkZjk3NGM0Y2FhM2JjYWIxODMxMzViNjkgPSAkKCc8ZGl2IGlkPSJodG1sX2NkNjA2ZGYzZGY5NzRjNGNhYTNiY2FiMTgzMTM1YjY5IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5XaWxsb3dkYWxlIFdlc3QsIE5vcnRoIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2UyYjNiOWNmNDg3YjRiMjNiOGRlY2ViZDA3OTRmODdiLnNldENvbnRlbnQoaHRtbF9jZDYwNmRmM2RmOTc0YzRjYWEzYmNhYjE4MzEzNWI2OSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9iOWZiYTEzNjc0NjY0YTllYTZjNmM2OTBlNjJiMmQ2OS5iaW5kUG9wdXAocG9wdXBfZTJiM2I5Y2Y0ODdiNGIyM2I4ZGVjZWJkMDc5NGY4N2IpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNjQzNTI1NTNhNDczNGE3YWI3Y2FiOWIwNjRjZDY4NmYgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43NTMyNTg2LC03OS4zMjk2NTY1XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzA1YzQxZTk2NjU1NTQxY2M5N2UzMGQwNDQyNTA4MDg0ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzQ5YmFhOTA5NzAwNDQyMjQ5NDhmMGM0ZTIyZWQ3ZTBjID0gJCgnPGRpdiBpZD0iaHRtbF80OWJhYTkwOTcwMDQ0MjI0OTQ4ZjBjNGUyMmVkN2UwYyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+UGFya3dvb2RzLCBOb3J0aCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8wNWM0MWU5NjY1NTU0MWNjOTdlMzBkMDQ0MjUwODA4NC5zZXRDb250ZW50KGh0bWxfNDliYWE5MDk3MDA0NDIyNDk0OGYwYzRlMjJlZDdlMGMpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNjQzNTI1NTNhNDczNGE3YWI3Y2FiOWIwNjRjZDY4NmYuYmluZFBvcHVwKHBvcHVwXzA1YzQxZTk2NjU1NTQxY2M5N2UzMGQwNDQyNTA4MDg0KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2M1NzkxNTQyZWUxNTRkZTQ4ZDgyNmZmMjIwNjRjMDAwID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzQ1OTA1Nzk5OTk5OTk2LC03OS4zNTIxODhdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfZmRmZDE5YTMzODY1NGVlNWI2MmM5NzVmODQzNTI4Y2YgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYjUwZWFiODAxZDJkNDI3NjhkNmVjZTg4OTgzYTdiMzkgPSAkKCc8ZGl2IGlkPSJodG1sX2I1MGVhYjgwMWQyZDQyNzY4ZDZlY2U4ODk4M2E3YjM5IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Eb24gTWlsbHMgTm9ydGgsIE5vcnRoIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2ZkZmQxOWEzMzg2NTRlZTViNjJjOTc1Zjg0MzUyOGNmLnNldENvbnRlbnQoaHRtbF9iNTBlYWI4MDFkMmQ0Mjc2OGQ2ZWNlODg5ODNhN2IzOSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9jNTc5MTU0MmVlMTU0ZGU0OGQ4MjZmZjIyMDY0YzAwMC5iaW5kUG9wdXAocG9wdXBfZmRmZDE5YTMzODY1NGVlNWI2MmM5NzVmODQzNTI4Y2YpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfODVhMTI0MjM2NzQ1NDI2M2I2NmQ0ODZiYjEyMzVhNzggPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MjU4OTk3MDAwMDAwMSwtNzkuMzQwOTIzXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzZjOTIyY2EzZjhmZTRmMGM4ODI5YzExNzNjMTY1ZjVmID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzI1MzcwZjE4NzY4NDQwYTRiNDgwODgxZmNjNjUzYmYwID0gJCgnPGRpdiBpZD0iaHRtbF8yNTM3MGYxODc2ODQ0MGE0YjQ4MDg4MWZjYzY1M2JmMCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RmxlbWluZ2RvbiBQYXJrLCBEb24gTWlsbHMgU291dGgsIE5vcnRoIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzZjOTIyY2EzZjhmZTRmMGM4ODI5YzExNzNjMTY1ZjVmLnNldENvbnRlbnQoaHRtbF8yNTM3MGYxODc2ODQ0MGE0YjQ4MDg4MWZjYzY1M2JmMCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl84NWExMjQyMzY3NDU0MjYzYjY2ZDQ4NmJiMTIzNWE3OC5iaW5kUG9wdXAocG9wdXBfNmM5MjJjYTNmOGZlNGYwYzg4MjljMTE3M2MxNjVmNWYpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMDg4Y2Y1MDExYjlmNDYzNjkxNDVmMDJiYzNkYjg4OWIgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43NTQzMjgzLC03OS40NDIyNTkzXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2ZhNGUxZjkyYjE1NzRjMmJiMDhmNmE2N2I0YjNkNmMzID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzVkZjcwNjc3MWQzOTQ1YjM4YmUzOTE2MTUxYTNhNGI2ID0gJCgnPGRpdiBpZD0iaHRtbF81ZGY3MDY3NzFkMzk0NWIzOGJlMzkxNjE1MWEzYTRiNiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+QmF0aHVyc3QgTWFub3IsIERvd25zdmlldyBOb3J0aCwgV2lsc29uIEhlaWdodHMsIE5vcnRoIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2ZhNGUxZjkyYjE1NzRjMmJiMDhmNmE2N2I0YjNkNmMzLnNldENvbnRlbnQoaHRtbF81ZGY3MDY3NzFkMzk0NWIzOGJlMzkxNjE1MWEzYTRiNik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8wODhjZjUwMTFiOWY0NjM2OTE0NWYwMmJjM2RiODg5Yi5iaW5kUG9wdXAocG9wdXBfZmE0ZTFmOTJiMTU3NGMyYmIwOGY2YTY3YjRiM2Q2YzMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYjFlNmMxYTViNzgwNGRhMGI5M2Y1NzU2NjcyYjJjNTggPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43Njc5ODAzLC03OS40ODcyNjE5MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8xZjg1MDQ4MDdkMTM0MzkwYTllYTc5ZGU2ZDQ2OGNhMCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8zZmIxNTBmMzFmMGM0ZDc1OTkyYzgwMGZhNjUxODQzYSA9ICQoJzxkaXYgaWQ9Imh0bWxfM2ZiMTUwZjMxZjBjNGQ3NTk5MmM4MDBmYTY1MTg0M2EiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk5vcnRod29vZCBQYXJrLCBZb3JrIFVuaXZlcnNpdHksIE5vcnRoIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzFmODUwNDgwN2QxMzQzOTBhOWVhNzlkZTZkNDY4Y2EwLnNldENvbnRlbnQoaHRtbF8zZmIxNTBmMzFmMGM0ZDc1OTkyYzgwMGZhNjUxODQzYSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9iMWU2YzFhNWI3ODA0ZGEwYjkzZjU3NTY2NzJiMmM1OC5iaW5kUG9wdXAocG9wdXBfMWY4NTA0ODA3ZDEzNDM5MGE5ZWE3OWRlNmQ0NjhjYTApOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMGRlYTBkZWRhY2I5NGNjNGE5NmFhNWQwMWNjYTE2NzAgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43Mzc0NzMyMDAwMDAwMDQsLTc5LjQ2NDc2MzI5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2Q3MWVhZWFmZDZhYTRhODdiYmVmNmU3MjI0YzYyZTAzID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2RmNWE0M2Y3ZGQ5OTRmZTc4MmJiMzRiYTQ4N2MyODY1ID0gJCgnPGRpdiBpZD0iaHRtbF9kZjVhNDNmN2RkOTk0ZmU3ODJiYjM0YmE0ODdjMjg2NSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Q0ZCIFRvcm9udG8sIERvd25zdmlldyBFYXN0LCBOb3J0aCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9kNzFlYWVhZmQ2YWE0YTg3YmJlZjZlNzIyNGM2MmUwMy5zZXRDb250ZW50KGh0bWxfZGY1YTQzZjdkZDk5NGZlNzgyYmIzNGJhNDg3YzI4NjUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMGRlYTBkZWRhY2I5NGNjNGE5NmFhNWQwMWNjYTE2NzAuYmluZFBvcHVwKHBvcHVwX2Q3MWVhZWFmZDZhYTRhODdiYmVmNmU3MjI0YzYyZTAzKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzg5YmUwNGY0NWY1NjQxMjk5NjA3OTIzZTZkOWI3NDMxID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzM5MDE0NiwtNzkuNTA2OTQzNl0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9iYWVmNzMwM2Q3ZTY0ZjczYmVlZDQ1MDdjZDA0MzIyMCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9kYzUyZDYyYWNmOGY0MzY3YTY5ZTg1MWQ4NDQ3OWVlZCA9ICQoJzxkaXYgaWQ9Imh0bWxfZGM1MmQ2MmFjZjhmNDM2N2E2OWU4NTFkODQ0NzllZWQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkRvd25zdmlldyBXZXN0LCBOb3J0aCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9iYWVmNzMwM2Q3ZTY0ZjczYmVlZDQ1MDdjZDA0MzIyMC5zZXRDb250ZW50KGh0bWxfZGM1MmQ2MmFjZjhmNDM2N2E2OWU4NTFkODQ0NzllZWQpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfODliZTA0ZjQ1ZjU2NDEyOTk2MDc5MjNlNmQ5Yjc0MzEuYmluZFBvcHVwKHBvcHVwX2JhZWY3MzAzZDdlNjRmNzNiZWVkNDUwN2NkMDQzMjIwKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2IzMWI5YTU0YmEyOTQyN2VhMTNmZTY1NTFlMWIxMWY4ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzI4NDk2NCwtNzkuNDk1Njk3NDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMTgzNTk2OTFjMDVjNDhiZDgyZThjMjBmZjc2ZjMxNjggPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMjY2N2M0OTE2MGQxNGU2YTlmNjczMWUwNGE1OGU3ZWIgPSAkKCc8ZGl2IGlkPSJodG1sXzI2NjdjNDkxNjBkMTRlNmE5ZjY3MzFlMDRhNThlN2ViIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Eb3duc3ZpZXcgQ2VudHJhbCwgTm9ydGggWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMTgzNTk2OTFjMDVjNDhiZDgyZThjMjBmZjc2ZjMxNjguc2V0Q29udGVudChodG1sXzI2NjdjNDkxNjBkMTRlNmE5ZjY3MzFlMDRhNThlN2ViKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2IzMWI5YTU0YmEyOTQyN2VhMTNmZTY1NTFlMWIxMWY4LmJpbmRQb3B1cChwb3B1cF8xODM1OTY5MWMwNWM0OGJkODJlOGMyMGZmNzZmMzE2OCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9mNWM0MjcwNDQxMDA0NzA5OTM1ODRlOGEzMzMzZGRkNyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc2MTYzMTMsLTc5LjUyMDk5OTQwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzVjYjdjNzRjOGI2ODQ3NjQ4ZTA5N2I4YWE1YjMyN2NmID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzA0YTZmNWNjN2EzYTQwMWM4NTUwODljYWUyZTYwOTc1ID0gJCgnPGRpdiBpZD0iaHRtbF8wNGE2ZjVjYzdhM2E0MDFjODU1MDg5Y2FlMmU2MDk3NSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RG93bnN2aWV3IE5vcnRod2VzdCwgTm9ydGggWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNWNiN2M3NGM4YjY4NDc2NDhlMDk3YjhhYTViMzI3Y2Yuc2V0Q29udGVudChodG1sXzA0YTZmNWNjN2EzYTQwMWM4NTUwODljYWUyZTYwOTc1KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2Y1YzQyNzA0NDEwMDQ3MDk5MzU4NGU4YTMzMzNkZGQ3LmJpbmRQb3B1cChwb3B1cF81Y2I3Yzc0YzhiNjg0NzY0OGUwOTdiOGFhNWIzMjdjZik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl82YTI5Y2NjZTIwZWM0OTEzOTM4MzZhN2Y3MTgwNmY1MyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcyNTg4MjI5OTk5OTk5NSwtNzkuMzE1NTcxNTk5OTk5OThdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfN2Y3ZDRlYzYwNjJkNGZjZWI3MjMzZTZiMmIwOTM0MGIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfZWIxYzhkNDgyM2M1NGM2M2E0NjUxMjUyYWM2MzgwOGEgPSAkKCc8ZGl2IGlkPSJodG1sX2ViMWM4ZDQ4MjNjNTRjNjNhNDY1MTI1MmFjNjM4MDhhIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5WaWN0b3JpYSBWaWxsYWdlLCBOb3J0aCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF83ZjdkNGVjNjA2MmQ0ZmNlYjcyMzNlNmIyYjA5MzQwYi5zZXRDb250ZW50KGh0bWxfZWIxYzhkNDgyM2M1NGM2M2E0NjUxMjUyYWM2MzgwOGEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNmEyOWNjY2UyMGVjNDkxMzkzODM2YTdmNzE4MDZmNTMuYmluZFBvcHVwKHBvcHVwXzdmN2Q0ZWM2MDYyZDRmY2ViNzIzM2U2YjJiMDkzNDBiKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzZhYTIzM2U0N2FjYjQ1NDk4ZDc1MDNlOGIxYmI1YjU5ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzA2Mzk3MiwtNzkuMzA5OTM3XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzNjNjM1MzhkZWJjNDRjZGU4ODA5NjYzMTRlOTE2MWExID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2YzOWZmZjUzZGY0NTQxZGY4MjE2NzQ0NWE5OTc5MDg5ID0gJCgnPGRpdiBpZD0iaHRtbF9mMzlmZmY1M2RmNDU0MWRmODIxNjc0NDVhOTk3OTA4OSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V29vZGJpbmUgR2FyZGVucywgUGFya3ZpZXcgSGlsbCwgRWFzdCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8zYzYzNTM4ZGViYzQ0Y2RlODgwOTY2MzE0ZTkxNjFhMS5zZXRDb250ZW50KGh0bWxfZjM5ZmZmNTNkZjQ1NDFkZjgyMTY3NDQ1YTk5NzkwODkpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNmFhMjMzZTQ3YWNiNDU0OThkNzUwM2U4YjFiYjViNTkuYmluZFBvcHVwKHBvcHVwXzNjNjM1MzhkZWJjNDRjZGU4ODA5NjYzMTRlOTE2MWExKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzgwMGM0NDA2MDM2NjQ4NDM5ZGYyZTY1MWE0NGMxMjM2ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjk1MzQzOTAwMDAwMDA1LC03OS4zMTgzODg3XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzY5YmY3MjIzOTgzZDQ2MDliZDhmYjg0MTA4MGFiYTgyID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzlkNmZhNDA3Mzk4OTQ1OWM4YTJhNTA2ODE5YTYxZjFlID0gJCgnPGRpdiBpZD0iaHRtbF85ZDZmYTQwNzM5ODk0NTljOGEyYTUwNjgxOWE2MWYxZSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V29vZGJpbmUgSGVpZ2h0cywgRWFzdCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF82OWJmNzIyMzk4M2Q0NjA5YmQ4ZmI4NDEwODBhYmE4Mi5zZXRDb250ZW50KGh0bWxfOWQ2ZmE0MDczOTg5NDU5YzhhMmE1MDY4MTlhNjFmMWUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfODAwYzQ0MDYwMzY2NDg0MzlkZjJlNjUxYTQ0YzEyMzYuYmluZFBvcHVwKHBvcHVwXzY5YmY3MjIzOTgzZDQ2MDliZDhmYjg0MTA4MGFiYTgyKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzkwMzY3Yzg2ODQ3MDQ5NWZiOTRlNWJlYzVmZTdlZTMzID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjc2MzU3Mzk5OTk5OTksLTc5LjI5MzAzMTJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYTM0OTk4Y2UyZTE2NGZkYjliZDhjYzhkNzJjYmQwODkgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfODgyM2M3NmQ5MzE5NGYwNzliNmM0NDIxMWIyMjc0N2EgPSAkKCc8ZGl2IGlkPSJodG1sXzg4MjNjNzZkOTMxOTRmMDc5YjZjNDQyMTFiMjI3NDdhIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5UaGUgQmVhY2hlcywgRWFzdCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9hMzQ5OThjZTJlMTY0ZmRiOWJkOGNjOGQ3MmNiZDA4OS5zZXRDb250ZW50KGh0bWxfODgyM2M3NmQ5MzE5NGYwNzliNmM0NDIxMWIyMjc0N2EpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfOTAzNjdjODY4NDcwNDk1ZmI5NGU1YmVjNWZlN2VlMzMuYmluZFBvcHVwKHBvcHVwX2EzNDk5OGNlMmUxNjRmZGI5YmQ4Y2M4ZDcyY2JkMDg5KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2ZhOGEyZDY3YjQ5ZjQxMjdhMmU2MjA4ODUyMTE1YmY4ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzA5MDYwNCwtNzkuMzYzNDUxN10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9kNDIyNmM2ODYxZTU0MTExYWU5NzE3YjM5YjM1ZmIzZCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9iMWNhMGI5M2YwMTM0ODExOTY3ZGU0MmU3ODkwYzUyMyA9ICQoJzxkaXYgaWQ9Imh0bWxfYjFjYTBiOTNmMDEzNDgxMTk2N2RlNDJlNzg5MGM1MjMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkxlYXNpZGUsIEVhc3QgWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZDQyMjZjNjg2MWU1NDExMWFlOTcxN2IzOWIzNWZiM2Quc2V0Q29udGVudChodG1sX2IxY2EwYjkzZjAxMzQ4MTE5NjdkZTQyZTc4OTBjNTIzKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2ZhOGEyZDY3YjQ5ZjQxMjdhMmU2MjA4ODUyMTE1YmY4LmJpbmRQb3B1cChwb3B1cF9kNDIyNmM2ODYxZTU0MTExYWU5NzE3YjM5YjM1ZmIzZCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8xNTliZWRmNzgyYzI0ZmJmYTU4NmMyY2VlMGVkNDUwYSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcwNTM2ODksLTc5LjM0OTM3MTkwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2JmMTEyYzM4YzljMTQ2M2E4ZjZiNzRkNThlZmVjZDlkID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2U1M2Y0MjhhYTUxMTQwMWVhODE0OTdhYWIwOGNkNGY0ID0gJCgnPGRpdiBpZD0iaHRtbF9lNTNmNDI4YWE1MTE0MDFlYTgxNDk3YWFiMDhjZDRmNCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+VGhvcm5jbGlmZmUgUGFyaywgRWFzdCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9iZjExMmMzOGM5YzE0NjNhOGY2Yjc0ZDU4ZWZlY2Q5ZC5zZXRDb250ZW50KGh0bWxfZTUzZjQyOGFhNTExNDAxZWE4MTQ5N2FhYjA4Y2Q0ZjQpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMTU5YmVkZjc4MmMyNGZiZmE1ODZjMmNlZTBlZDQ1MGEuYmluZFBvcHVwKHBvcHVwX2JmMTEyYzM4YzljMTQ2M2E4ZjZiNzRkNThlZmVjZDlkKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzQxMTljMmNkNDUzMDQxNDFhMWIzNDgwZGIyYzk2MzVlID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjg1MzQ3LC03OS4zMzgxMDY1XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzExNDYxZTFkODgxNTRhMDFiYWZhNzg5Y2I1ZjM3YmNhID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzEzMzQ5ZjlmMmM0NTRhOWFhZmQwZDA1Yjk3MjViY2M1ID0gJCgnPGRpdiBpZD0iaHRtbF8xMzM0OWY5ZjJjNDU0YTlhYWZkMGQwNWI5NzI1YmNjNSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RWFzdCBUb3JvbnRvLCBFYXN0IFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzExNDYxZTFkODgxNTRhMDFiYWZhNzg5Y2I1ZjM3YmNhLnNldENvbnRlbnQoaHRtbF8xMzM0OWY5ZjJjNDU0YTlhYWZkMGQwNWI5NzI1YmNjNSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl80MTE5YzJjZDQ1MzA0MTQxYTFiMzQ4MGRiMmM5NjM1ZS5iaW5kUG9wdXAocG9wdXBfMTE0NjFlMWQ4ODE1NGEwMWJhZmE3ODljYjVmMzdiY2EpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOTA2OWJlOTZjZmZjNDI4NDg3MzMzOWJjMDAzYWE3NGEgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42Nzk1NTcxLC03OS4zNTIxODhdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfNTNmOTgyMjY0ZDJiNGVhYmJhYTdkNTJiOWIyOWRiYjIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMmViZTQwMTg1MTcyNGE2ZThkZjY0Mjk3MWE1NmZiZDkgPSAkKCc8ZGl2IGlkPSJodG1sXzJlYmU0MDE4NTE3MjRhNmU4ZGY2NDI5NzFhNTZmYmQ5IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5UaGUgRGFuZm9ydGggV2VzdCwgUml2ZXJkYWxlLCBFYXN0IFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzUzZjk4MjI2NGQyYjRlYWJiYWE3ZDUyYjliMjlkYmIyLnNldENvbnRlbnQoaHRtbF8yZWJlNDAxODUxNzI0YTZlOGRmNjQyOTcxYTU2ZmJkOSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl85MDY5YmU5NmNmZmM0Mjg0ODczMzM5YmMwMDNhYTc0YS5iaW5kUG9wdXAocG9wdXBfNTNmOTgyMjY0ZDJiNGVhYmJhYTdkNTJiOWIyOWRiYjIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYzJlNDM1NmNjYTExNDEyOGEwMmU4MDc4ZWMxYzljZDIgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42Njg5OTg1LC03OS4zMTU1NzE1OTk5OTk5OF0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8yNTk1ZjAzOTdhMmQ0OGY5ODRhODU2M2E5MTI2M2EzNCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8yNGE0N2JiYjZmODY0Y2U0ODMzZjYwMzViY2E4NmQ3ZCA9ICQoJzxkaXYgaWQ9Imh0bWxfMjRhNDdiYmI2Zjg2NGNlNDgzM2Y2MDM1YmNhODZkN2QiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlRoZSBCZWFjaGVzIFdlc3QsIEluZGlhIEJhemFhciwgRWFzdCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8yNTk1ZjAzOTdhMmQ0OGY5ODRhODU2M2E5MTI2M2EzNC5zZXRDb250ZW50KGh0bWxfMjRhNDdiYmI2Zjg2NGNlNDgzM2Y2MDM1YmNhODZkN2QpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYzJlNDM1NmNjYTExNDEyOGEwMmU4MDc4ZWMxYzljZDIuYmluZFBvcHVwKHBvcHVwXzI1OTVmMDM5N2EyZDQ4Zjk4NGE4NTYzYTkxMjYzYTM0KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzZkNGVhNjFhMTE1YzQ5Nzk4YmNmMGFlMTYxOTAzNzhlID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjU5NTI1NSwtNzkuMzQwOTIzXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2ZlYTVhMTU2MTkxMTQ2YTRhY2M2NzZkZmVkMGZkNjJlID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2JiOGI1ZjFmYTNkYzQyNTA5MTdlOTdiNjIyNzY3MzY0ID0gJCgnPGRpdiBpZD0iaHRtbF9iYjhiNWYxZmEzZGM0MjUwOTE3ZTk3YjYyMjc2NzM2NCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+U3R1ZGlvIERpc3RyaWN0LCBFYXN0IFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2ZlYTVhMTU2MTkxMTQ2YTRhY2M2NzZkZmVkMGZkNjJlLnNldENvbnRlbnQoaHRtbF9iYjhiNWYxZmEzZGM0MjUwOTE3ZTk3YjYyMjc2NzM2NCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl82ZDRlYTYxYTExNWM0OTc5OGJjZjBhZTE2MTkwMzc4ZS5iaW5kUG9wdXAocG9wdXBfZmVhNWExNTYxOTExNDZhNGFjYzY3NmRmZWQwZmQ2MmUpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMDQ2ZDZlOTdkYzY4NDM2Mzg2OTEzM2U1ZjcwOGYwMWEgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MjgwMjA1LC03OS4zODg3OTAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2NkZTMwNTFjOTVmNjRhMGY5NDgzMGFkY2Y2MjE2YWE4ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzJiNjgwMTJlZmNhODRhNmFhMzNlNzljMTAwYmU1MDAwID0gJCgnPGRpdiBpZD0iaHRtbF8yYjY4MDEyZWZjYTg0YTZhYTMzZTc5YzEwMGJlNTAwMCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TGF3cmVuY2UgUGFyaywgQ2VudHJhbCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9jZGUzMDUxYzk1ZjY0YTBmOTQ4MzBhZGNmNjIxNmFhOC5zZXRDb250ZW50KGh0bWxfMmI2ODAxMmVmY2E4NGE2YWEzM2U3OWMxMDBiZTUwMDApOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMDQ2ZDZlOTdkYzY4NDM2Mzg2OTEzM2U1ZjcwOGYwMWEuYmluZFBvcHVwKHBvcHVwX2NkZTMwNTFjOTVmNjRhMGY5NDgzMGFkY2Y2MjE2YWE4KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2VmYzM3NzZhZTAxZTQ4Zjk5OTdhODMyYzE2NDBjYmZiID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzEyNzUxMSwtNzkuMzkwMTk3NV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9mYWI3NDY4ODRlZjI0N2U3YTU2MzQwYjU5MWYyZDJjZiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8zNjM3NDg0MDIxMjc0MzY2OGNiNWE2OWY2NmVkNjM5OSA9ICQoJzxkaXYgaWQ9Imh0bWxfMzYzNzQ4NDAyMTI3NDM2NjhjYjVhNjlmNjZlZDYzOTkiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkRhdmlzdmlsbGUgTm9ydGgsIENlbnRyYWwgVG9yb250bzwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZmFiNzQ2ODg0ZWYyNDdlN2E1NjM0MGI1OTFmMmQyY2Yuc2V0Q29udGVudChodG1sXzM2Mzc0ODQwMjEyNzQzNjY4Y2I1YTY5ZjY2ZWQ2Mzk5KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2VmYzM3NzZhZTAxZTQ4Zjk5OTdhODMyYzE2NDBjYmZiLmJpbmRQb3B1cChwb3B1cF9mYWI3NDY4ODRlZjI0N2U3YTU2MzQwYjU5MWYyZDJjZik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl81YzA4ZWMyZDljNTE0OGVlYjVlN2I2Y2M2MzA4NWU4NSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcxNTM4MzQsLTc5LjQwNTY3ODQwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzkzM2YzYTA0NWE3ZjQ0NzZiZDFhY2YzM2NmMWFmZTY5ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzBlYjllNjRmZmM3YjQxMjJiYmYwZjQzZmJmYTNlMWIxID0gJCgnPGRpdiBpZD0iaHRtbF8wZWI5ZTY0ZmZjN2I0MTIyYmJmMGY0M2ZiZmEzZTFiMSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Tm9ydGggVG9yb250byBXZXN0LCBDZW50cmFsIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzkzM2YzYTA0NWE3ZjQ0NzZiZDFhY2YzM2NmMWFmZTY5LnNldENvbnRlbnQoaHRtbF8wZWI5ZTY0ZmZjN2I0MTIyYmJmMGY0M2ZiZmEzZTFiMSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl81YzA4ZWMyZDljNTE0OGVlYjVlN2I2Y2M2MzA4NWU4NS5iaW5kUG9wdXAocG9wdXBfOTMzZjNhMDQ1YTdmNDQ3NmJkMWFjZjMzY2YxYWZlNjkpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYjA3NGEzNmIzZjE2NDhjY2I2OGVjZWRiZmIxMGQ2MGYgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MDQzMjQ0LC03OS4zODg3OTAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzU0MDFhYmIyZWE1OTQ4MWFiZDQ2MWNiYmI0NDQwODljID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzlmMzMxOWFlYjg0MTQyYzdiYWFiYzgyYjVmMGZmNDVhID0gJCgnPGRpdiBpZD0iaHRtbF85ZjMzMTlhZWI4NDE0MmM3YmFhYmM4MmI1ZjBmZjQ1YSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RGF2aXN2aWxsZSwgQ2VudHJhbCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF81NDAxYWJiMmVhNTk0ODFhYmQ0NjFjYmJiNDQ0MDg5Yy5zZXRDb250ZW50KGh0bWxfOWYzMzE5YWViODQxNDJjN2JhYWJjODJiNWYwZmY0NWEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYjA3NGEzNmIzZjE2NDhjY2I2OGVjZWRiZmIxMGQ2MGYuYmluZFBvcHVwKHBvcHVwXzU0MDFhYmIyZWE1OTQ4MWFiZDQ2MWNiYmI0NDQwODljKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2I5MWFhNDdhZDY1OTQ0N2E5YTcxZTEyN2YwNDcyM2FjID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjg5NTc0MywtNzkuMzgzMTU5OTAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfN2QxYjQwMzA5OTkxNDQ1ZjlmMTQ4M2YwYjc4ZWU0YTYgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNGZiNGNmNDEyZjNiNGQwNjgzNjg1NDliY2EyZWMyNWIgPSAkKCc8ZGl2IGlkPSJodG1sXzRmYjRjZjQxMmYzYjRkMDY4MzY4NTQ5YmNhMmVjMjViIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Nb29yZSBQYXJrLCBTdW1tZXJoaWxsIEVhc3QsIENlbnRyYWwgVG9yb250bzwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfN2QxYjQwMzA5OTkxNDQ1ZjlmMTQ4M2YwYjc4ZWU0YTYuc2V0Q29udGVudChodG1sXzRmYjRjZjQxMmYzYjRkMDY4MzY4NTQ5YmNhMmVjMjViKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2I5MWFhNDdhZDY1OTQ0N2E5YTcxZTEyN2YwNDcyM2FjLmJpbmRQb3B1cChwb3B1cF83ZDFiNDAzMDk5OTE0NDVmOWYxNDgzZjBiNzhlZTRhNik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8xZDY0MjczZTgzMjQ0ODViODhlMmU1ZWRjYzE2ZmUxNiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY4NjQxMjI5OTk5OTk5LC03OS40MDAwNDkzXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzYzOTg4MzJiNzc1MDRlMGJhYTBkOGI0YjU1OGIxNWRjID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzJlMTg5YTI5MzExMDQ5ODVhOWQ4NTc5N2U3NDM1Y2Y4ID0gJCgnPGRpdiBpZD0iaHRtbF8yZTE4OWEyOTMxMTA0OTg1YTlkODU3OTdlNzQzNWNmOCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RGVlciBQYXJrLCBGb3Jlc3QgSGlsbCBTRSwgUmF0aG5lbGx5LCBTb3V0aCBIaWxsLCBTdW1tZXJoaWxsIFdlc3QsIENlbnRyYWwgVG9yb250bzwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNjM5ODgzMmI3NzUwNGUwYmFhMGQ4YjRiNTU4YjE1ZGMuc2V0Q29udGVudChodG1sXzJlMTg5YTI5MzExMDQ5ODVhOWQ4NTc5N2U3NDM1Y2Y4KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzFkNjQyNzNlODMyNDQ4NWI4OGUyZTVlZGNjMTZmZTE2LmJpbmRQb3B1cChwb3B1cF82Mzk4ODMyYjc3NTA0ZTBiYWEwZDhiNGI1NThiMTVkYyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9kYmVhNTY0MmM1ODg0NjhhOTM2ZTQ2ZGM3Y2UzNGUxMCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY3OTU2MjYsLTc5LjM3NzUyOTQwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzQ2YTFiOWZkZTcwOTRjNzM4NDk2NzNjZTEyZDZmMDhkID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2E5MjI5YTQwMmE1YzQ4ODBhMmJiNDFjZmNjNDgzNTI4ID0gJCgnPGRpdiBpZD0iaHRtbF9hOTIyOWE0MDJhNWM0ODgwYTJiYjQxY2ZjYzQ4MzUyOCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Um9zZWRhbGUsIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzQ2YTFiOWZkZTcwOTRjNzM4NDk2NzNjZTEyZDZmMDhkLnNldENvbnRlbnQoaHRtbF9hOTIyOWE0MDJhNWM0ODgwYTJiYjQxY2ZjYzQ4MzUyOCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9kYmVhNTY0MmM1ODg0NjhhOTM2ZTQ2ZGM3Y2UzNGUxMC5iaW5kUG9wdXAocG9wdXBfNDZhMWI5ZmRlNzA5NGM3Mzg0OTY3M2NlMTJkNmYwOGQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYjZhMWI1ZjM1M2NjNGMwOTliNzVmNDNkNGNiNjMwMzYgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42Njc5NjcsLTc5LjM2NzY3NTNdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYjZlNTFkYTFmZTdiNDZmNGI1MmYxNjRhOWY2OGMwODMgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfZDJkZTY2YzZiYjY5NGY5NWE2MmUwZGRiYmM3Mjk5NDAgPSAkKCc8ZGl2IGlkPSJodG1sX2QyZGU2NmM2YmI2OTRmOTVhNjJlMGRkYmJjNzI5OTQwIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5DYWJiYWdldG93biwgU3QuIEphbWVzIFRvd24sIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2I2ZTUxZGExZmU3YjQ2ZjRiNTJmMTY0YTlmNjhjMDgzLnNldENvbnRlbnQoaHRtbF9kMmRlNjZjNmJiNjk0Zjk1YTYyZTBkZGJiYzcyOTk0MCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9iNmExYjVmMzUzY2M0YzA5OWI3NWY0M2Q0Y2I2MzAzNi5iaW5kUG9wdXAocG9wdXBfYjZlNTFkYTFmZTdiNDZmNGI1MmYxNjRhOWY2OGMwODMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOTc5NjQxNDVkMzFhNDg4M2JlOWZiYWQ4ZWUxZGE4MmMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NjU4NTk5LC03OS4zODMxNTk5MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9kMTQ4YzUyN2MxZmI0ODVjODVhMTczNDRiMjE2NzFhNSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9mNGI5ZGQzNTEwYmI0MDVhYmVhNjlmZTNiODA4MzYwZiA9ICQoJzxkaXYgaWQ9Imh0bWxfZjRiOWRkMzUxMGJiNDA1YWJlYTY5ZmUzYjgwODM2MGYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNodXJjaCBhbmQgV2VsbGVzbGV5LCBEb3dudG93biBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9kMTQ4YzUyN2MxZmI0ODVjODVhMTczNDRiMjE2NzFhNS5zZXRDb250ZW50KGh0bWxfZjRiOWRkMzUxMGJiNDA1YWJlYTY5ZmUzYjgwODM2MGYpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfOTc5NjQxNDVkMzFhNDg4M2JlOWZiYWQ4ZWUxZGE4MmMuYmluZFBvcHVwKHBvcHVwX2QxNDhjNTI3YzFmYjQ4NWM4NWExNzM0NGIyMTY3MWE1KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzBjZTQ0N2YzZWJjYTQ0MGRiNjQ4MTIyNmVjYTk0M2M1ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjU0MjU5OSwtNzkuMzYwNjM1OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF82ZDdjMGY5ZGYyODM0YzYzOGQzN2I0NDhhZmEwZTgwZiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF82M2JhMGI1OTZhNWI0ZDAwODZiYzBiMDFjYWExMGZiOSA9ICQoJzxkaXYgaWQ9Imh0bWxfNjNiYTBiNTk2YTViNGQwMDg2YmMwYjAxY2FhMTBmYjkiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkhhcmJvdXJmcm9udCwgRG93bnRvd24gVG9yb250bzwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNmQ3YzBmOWRmMjgzNGM2MzhkMzdiNDQ4YWZhMGU4MGYuc2V0Q29udGVudChodG1sXzYzYmEwYjU5NmE1YjRkMDA4NmJjMGIwMWNhYTEwZmI5KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzBjZTQ0N2YzZWJjYTQ0MGRiNjQ4MTIyNmVjYTk0M2M1LmJpbmRQb3B1cChwb3B1cF82ZDdjMGY5ZGYyODM0YzYzOGQzN2I0NDhhZmEwZTgwZik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9iMGQyOTQ0N2I4NWM0NTgzYTc3YzE5NTUyMzhlM2E2ZiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY1NzE2MTgsLTc5LjM3ODkzNzA5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2E3Mzc1NjM5YTU5ODRlY2M4OTM3NzY5MjkzNzIwYmY2ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzg1NTU5NTlhOTYyZTRmZDg5ZjQ2ZTE4ZDYwMmJmNjdhID0gJCgnPGRpdiBpZD0iaHRtbF84NTU1OTU5YTk2MmU0ZmQ4OWY0NmUxOGQ2MDJiZjY3YSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+UnllcnNvbiwgR2FyZGVuIERpc3RyaWN0LCBEb3dudG93biBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9hNzM3NTYzOWE1OTg0ZWNjODkzNzc2OTI5MzcyMGJmNi5zZXRDb250ZW50KGh0bWxfODU1NTk1OWE5NjJlNGZkODlmNDZlMThkNjAyYmY2N2EpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYjBkMjk0NDdiODVjNDU4M2E3N2MxOTU1MjM4ZTNhNmYuYmluZFBvcHVwKHBvcHVwX2E3Mzc1NjM5YTU5ODRlY2M4OTM3NzY5MjkzNzIwYmY2KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzc4YmU1Y2JmZjk4ZjQ4YmZhMDdhMzFhNGE1MjI5ZTY5ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjUxNDkzOSwtNzkuMzc1NDE3OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF83OGY2MTMyODBjYmU0NWNiYjQ0NWJjZGYwNDdkZjFlYyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF83Mzg3YTYyZTQ2NDc0ZWQwODMzMTdmZTlkMTkxYjllMCA9ICQoJzxkaXYgaWQ9Imh0bWxfNzM4N2E2MmU0NjQ3NGVkMDgzMzE3ZmU5ZDE5MWI5ZTAiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlN0LiBKYW1lcyBUb3duLCBEb3dudG93biBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF83OGY2MTMyODBjYmU0NWNiYjQ0NWJjZGYwNDdkZjFlYy5zZXRDb250ZW50KGh0bWxfNzM4N2E2MmU0NjQ3NGVkMDgzMzE3ZmU5ZDE5MWI5ZTApOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNzhiZTVjYmZmOThmNDhiZmEwN2EzMWE0YTUyMjllNjkuYmluZFBvcHVwKHBvcHVwXzc4ZjYxMzI4MGNiZTQ1Y2JiNDQ1YmNkZjA0N2RmMWVjKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2I4ZjBmN2ZjZGM5YTQyOTg4ZDIxYzA5ZTUzYzkyZGJkID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjQ0NzcwNzk5OTk5OTk2LC03OS4zNzMzMDY0XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2YxY2I0MmRmNGVhOTQ1ZTc4ZjE2ODk3ZTFlNzE2ZDU0ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzU1NjMyM2IwYzYxMzQ3Mjk4NzczMjRmNmI5MTZmMDM2ID0gJCgnPGRpdiBpZD0iaHRtbF81NTYzMjNiMGM2MTM0NzI5ODc3MzI0ZjZiOTE2ZjAzNiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+QmVyY3p5IFBhcmssIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2YxY2I0MmRmNGVhOTQ1ZTc4ZjE2ODk3ZTFlNzE2ZDU0LnNldENvbnRlbnQoaHRtbF81NTYzMjNiMGM2MTM0NzI5ODc3MzI0ZjZiOTE2ZjAzNik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9iOGYwZjdmY2RjOWE0Mjk4OGQyMWMwOWU1M2M5MmRiZC5iaW5kUG9wdXAocG9wdXBfZjFjYjQyZGY0ZWE5NDVlNzhmMTY4OTdlMWU3MTZkNTQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYTcwMTNjMTgzZjRiNDA5NDk2ZWMxZWZlMGZlYWMzOGMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NTc5NTI0LC03OS4zODczODI2XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzUxNTIzNDg0MzExYTRiYjRhMzBmYTBmNmU2ZjIwMjg0ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzgxZDMyOGJiNGFmYzQ3MWE4OWM0YzJkZTMwOTgwNDhkID0gJCgnPGRpdiBpZD0iaHRtbF84MWQzMjhiYjRhZmM0NzFhODljNGMyZGUzMDk4MDQ4ZCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Q2VudHJhbCBCYXkgU3RyZWV0LCBEb3dudG93biBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF81MTUyMzQ4NDMxMWE0YmI0YTMwZmEwZjZlNmYyMDI4NC5zZXRDb250ZW50KGh0bWxfODFkMzI4YmI0YWZjNDcxYTg5YzRjMmRlMzA5ODA0OGQpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYTcwMTNjMTgzZjRiNDA5NDk2ZWMxZWZlMGZlYWMzOGMuYmluZFBvcHVwKHBvcHVwXzUxNTIzNDg0MzExYTRiYjRhMzBmYTBmNmU2ZjIwMjg0KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2Q5NTlmODA3YmExZjRjYWNiZmY2ODBhZTMwMjAxMDMxID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjUwNTcxMjAwMDAwMDEsLTc5LjM4NDU2NzVdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMjExY2JiM2ZlNGUxNGY0NDk2NDc5NjQ2ZWU5OWUxZDQgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYTA4NDFkYzI0MDA0NGE1NmEzYjYxMDAyNDc3NTgzYTMgPSAkKCc8ZGl2IGlkPSJodG1sX2EwODQxZGMyNDAwNDRhNTZhM2I2MTAwMjQ3NzU4M2EzIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5BZGVsYWlkZSwgS2luZywgUmljaG1vbmQsIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzIxMWNiYjNmZTRlMTRmNDQ5NjQ3OTY0NmVlOTllMWQ0LnNldENvbnRlbnQoaHRtbF9hMDg0MWRjMjQwMDQ0YTU2YTNiNjEwMDI0Nzc1ODNhMyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9kOTU5ZjgwN2JhMWY0Y2FjYmZmNjgwYWUzMDIwMTAzMS5iaW5kUG9wdXAocG9wdXBfMjExY2JiM2ZlNGUxNGY0NDk2NDc5NjQ2ZWU5OWUxZDQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNzA5MTdjMjc1NzEyNGViZjliZWYzYTQ3ZDZhNjIyYTMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDA4MTU3LC03OS4zODE3NTIyOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9jM2MxYmRlNmM1N2Y0NWQzYjI2N2QxMDZkMDFiOWY2ZCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8zOWNjYzAxZjM2Nzk0MTVjYWYwNTM4Njc5MGFmZjRhMCA9ICQoJzxkaXYgaWQ9Imh0bWxfMzljY2MwMWYzNjc5NDE1Y2FmMDUzODY3OTBhZmY0YTAiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkhhcmJvdXJmcm9udCBFYXN0LCBUb3JvbnRvIElzbGFuZHMsIFVuaW9uIFN0YXRpb24sIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2MzYzFiZGU2YzU3ZjQ1ZDNiMjY3ZDEwNmQwMWI5ZjZkLnNldENvbnRlbnQoaHRtbF8zOWNjYzAxZjM2Nzk0MTVjYWYwNTM4Njc5MGFmZjRhMCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl83MDkxN2MyNzU3MTI0ZWJmOWJlZjNhNDdkNmE2MjJhMy5iaW5kUG9wdXAocG9wdXBfYzNjMWJkZTZjNTdmNDVkM2IyNjdkMTA2ZDAxYjlmNmQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOGNmMjVkNDRjYjFmNGFkNGI5NGRkNGRiOWEyYjJkN2MgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDcxNzY4LC03OS4zODE1NzY0MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9iOGNiZTJkNWYwNjI0OTljYjg2MjZlNTUyMDYwYjhmMyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF82NjNhOTkyMGYzODc0MGJkYTYxNjkzNzI2MThkMWM0NiA9ICQoJzxkaXYgaWQ9Imh0bWxfNjYzYTk5MjBmMzg3NDBiZGE2MTY5MzcyNjE4ZDFjNDYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkRlc2lnbiBFeGNoYW5nZSwgVG9yb250byBEb21pbmlvbiBDZW50cmUsIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2I4Y2JlMmQ1ZjA2MjQ5OWNiODYyNmU1NTIwNjBiOGYzLnNldENvbnRlbnQoaHRtbF82NjNhOTkyMGYzODc0MGJkYTYxNjkzNzI2MThkMWM0Nik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl84Y2YyNWQ0NGNiMWY0YWQ0Yjk0ZGQ0ZGI5YTJiMmQ3Yy5iaW5kUG9wdXAocG9wdXBfYjhjYmUyZDVmMDYyNDk5Y2I4NjI2ZTU1MjA2MGI4ZjMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMGM1ZGU0NGRjMjMzNDIyNWE1OGJmODkwNTBkYTM4NjIgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDgxOTg1LC03OS4zNzk4MTY5MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF81ZmI0NGI0OTRhNjQ0MmE0OWJhMjdkZmFiNjc4MDg0MiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84NjdhYWJjZDE1ZTg0ODg1YTgwNzM0ZDY5NzAxNmE5YSA9ICQoJzxkaXYgaWQ9Imh0bWxfODY3YWFiY2QxNWU4NDg4NWE4MDczNGQ2OTcwMTZhOWEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNvbW1lcmNlIENvdXJ0LCBWaWN0b3JpYSBIb3RlbCwgRG93bnRvd24gVG9yb250bzwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNWZiNDRiNDk0YTY0NDJhNDliYTI3ZGZhYjY3ODA4NDIuc2V0Q29udGVudChodG1sXzg2N2FhYmNkMTVlODQ4ODVhODA3MzRkNjk3MDE2YTlhKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzBjNWRlNDRkYzIzMzQyMjVhNThiZjg5MDUwZGEzODYyLmJpbmRQb3B1cChwb3B1cF81ZmI0NGI0OTRhNjQ0MmE0OWJhMjdkZmFiNjc4MDg0Mik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl81OThiNDRiMDAzMzU0MDA4OTQ5ZWU1OWJlYjI4ZTRjMiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjczMzI4MjUsLTc5LjQxOTc0OTddLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMmJmMmY3ZDZjNTM3NDllMmIxMDM1Y2RjNzAzNmY5ZjMgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNWUxYmVkZmZhNzA4NDMxYjk0ZTZkYjY2MDhhMjQxOWEgPSAkKCc8ZGl2IGlkPSJodG1sXzVlMWJlZGZmYTcwODQzMWI5NGU2ZGI2NjA4YTI0MTlhIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5CZWRmb3JkIFBhcmssIExhd3JlbmNlIE1hbm9yIEVhc3QsIE5vcnRoIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzJiZjJmN2Q2YzUzNzQ5ZTJiMTAzNWNkYzcwMzZmOWYzLnNldENvbnRlbnQoaHRtbF81ZTFiZWRmZmE3MDg0MzFiOTRlNmRiNjYwOGEyNDE5YSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl81OThiNDRiMDAzMzU0MDA4OTQ5ZWU1OWJlYjI4ZTRjMi5iaW5kUG9wdXAocG9wdXBfMmJmMmY3ZDZjNTM3NDllMmIxMDM1Y2RjNzAzNmY5ZjMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOTM3NTYzNGYxZGE2NGQzNWEwOTU1NjM3ODVmOGYxNzEgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MTE2OTQ4LC03OS40MTY5MzU1OTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9hM2QyNWY4YWUxMjg0MDAyOTliOTA4YmIwZTNkOWFjYSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84YjQ3YWQ1Y2Y2MTc0MWZmOGVjYzZjMzYxNjgzNTZiYSA9ICQoJzxkaXYgaWQ9Imh0bWxfOGI0N2FkNWNmNjE3NDFmZjhlY2M2YzM2MTY4MzU2YmEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlJvc2VsYXduLCBDZW50cmFsIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2EzZDI1ZjhhZTEyODQwMDI5OWI5MDhiYjBlM2Q5YWNhLnNldENvbnRlbnQoaHRtbF84YjQ3YWQ1Y2Y2MTc0MWZmOGVjYzZjMzYxNjgzNTZiYSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl85Mzc1NjM0ZjFkYTY0ZDM1YTA5NTU2Mzc4NWY4ZjE3MS5iaW5kUG9wdXAocG9wdXBfYTNkMjVmOGFlMTI4NDAwMjk5YjkwOGJiMGUzZDlhY2EpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYWNiNTFkZWJmYzEwNDkzZGEwNzljZjFlNDZmNmRmYWMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42OTY5NDc2LC03OS40MTEzMDcyMDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8yN2RmYzM5ZTZjNTY0YzRiOTQyODk1YWFlOGJjYjJmMCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9jZTgxZTM1MzUzODI0NjFjOGNiZDAyNTczNDM1NmU1NCA9ICQoJzxkaXYgaWQ9Imh0bWxfY2U4MWUzNTM1MzgyNDYxYzhjYmQwMjU3MzQzNTZlNTQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkZvcmVzdCBIaWxsIE5vcnRoLCBGb3Jlc3QgSGlsbCBXZXN0LCBDZW50cmFsIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzI3ZGZjMzllNmM1NjRjNGI5NDI4OTVhYWU4YmNiMmYwLnNldENvbnRlbnQoaHRtbF9jZTgxZTM1MzUzODI0NjFjOGNiZDAyNTczNDM1NmU1NCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9hY2I1MWRlYmZjMTA0OTNkYTA3OWNmMWU0NmY2ZGZhYy5iaW5kUG9wdXAocG9wdXBfMjdkZmMzOWU2YzU2NGM0Yjk0Mjg5NWFhZThiY2IyZjApOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMmFhN2MxMzA2NmQ5NDVjNGE3YWY5NDQzNjRhNGQ3Y2EgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NzI3MDk3LC03OS40MDU2Nzg0MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8yZDI0Y2UwNDQzMjA0MjVhYWVmZjcwNzM5YzA3MzQ5MyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8zMWQ3YzhkNjBmZDE0OTFhYWMyYWUwZTdjZTViMmM1YSA9ICQoJzxkaXYgaWQ9Imh0bWxfMzFkN2M4ZDYwZmQxNDkxYWFjMmFlMGU3Y2U1YjJjNWEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlRoZSBBbm5leCwgTm9ydGggTWlkdG93biwgWW9ya3ZpbGxlLCBDZW50cmFsIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzJkMjRjZTA0NDMyMDQyNWFhZWZmNzA3MzljMDczNDkzLnNldENvbnRlbnQoaHRtbF8zMWQ3YzhkNjBmZDE0OTFhYWMyYWUwZTdjZTViMmM1YSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8yYWE3YzEzMDY2ZDk0NWM0YTdhZjk0NDM2NGE0ZDdjYS5iaW5kUG9wdXAocG9wdXBfMmQyNGNlMDQ0MzIwNDI1YWFlZmY3MDczOWMwNzM0OTMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMTMzZTNiYjVhMTJiNDJkMGFkYjI3ZjMwZDAwZDE2ZWUgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NjI2OTU2LC03OS40MDAwNDkzXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzQxODI1YWFkYTdkNzQxYzNhYWEzZTVkMmYwMjEyMzBkID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzhhYzA4OTUzYzcwODQ2N2Y5ZWUzZmZhNjFkZDA1M2U1ID0gJCgnPGRpdiBpZD0iaHRtbF84YWMwODk1M2M3MDg0NjdmOWVlM2ZmYTYxZGQwNTNlNSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+SGFyYm9yZCwgVW5pdmVyc2l0eSBvZiBUb3JvbnRvLCBEb3dudG93biBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF80MTgyNWFhZGE3ZDc0MWMzYWFhM2U1ZDJmMDIxMjMwZC5zZXRDb250ZW50KGh0bWxfOGFjMDg5NTNjNzA4NDY3ZjllZTNmZmE2MWRkMDUzZTUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMTMzZTNiYjVhMTJiNDJkMGFkYjI3ZjMwZDAwZDE2ZWUuYmluZFBvcHVwKHBvcHVwXzQxODI1YWFkYTdkNzQxYzNhYWEzZTVkMmYwMjEyMzBkKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzUyOGU0NDIxYTRkMTRkMjE5MDU5ZDA4ZTYyOTA4YzMxID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjUzMjA1NywtNzkuNDAwMDQ5M10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9iOTc5MGQ1NjI3NGQ0NjY1ODIxYTViOTU4YzVhZjJhYyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF83NGViN2YyNjU1M2E0MTUzOTY3NWEzMWNjYzJmMTNiYSA9ICQoJzxkaXYgaWQ9Imh0bWxfNzRlYjdmMjY1NTNhNDE1Mzk2NzVhMzFjY2MyZjEzYmEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNoaW5hdG93biwgR3JhbmdlIFBhcmssIEtlbnNpbmd0b24gTWFya2V0LCBEb3dudG93biBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9iOTc5MGQ1NjI3NGQ0NjY1ODIxYTViOTU4YzVhZjJhYy5zZXRDb250ZW50KGh0bWxfNzRlYjdmMjY1NTNhNDE1Mzk2NzVhMzFjY2MyZjEzYmEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNTI4ZTQ0MjFhNGQxNGQyMTkwNTlkMDhlNjI5MDhjMzEuYmluZFBvcHVwKHBvcHVwX2I5NzkwZDU2Mjc0ZDQ2NjU4MjFhNWI5NThjNWFmMmFjKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2RlZjZkNDE0OTM3NzRmYWFiMzM2NjIyYzg1MjNiZDBhID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjI4OTQ2NywtNzkuMzk0NDE5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF80ZWEzZmY5NDVkYWY0OTNlODdiYTc2YWIyYjllZjc2YSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF85MzkzODdkZTFlZjU0M2Q2YjVkY2ZkM2EzMGRkMDFmNiA9ICQoJzxkaXYgaWQ9Imh0bWxfOTM5Mzg3ZGUxZWY1NDNkNmI1ZGNmZDNhMzBkZDAxZjYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNOIFRvd2VyLCBCYXRodXJzdCBRdWF5LCBJc2xhbmQgYWlycG9ydCwgSGFyYm91cmZyb250IFdlc3QsIEtpbmcgYW5kIFNwYWRpbmEsIFJhaWx3YXkgTGFuZHMsIFNvdXRoIE5pYWdhcmEsIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzRlYTNmZjk0NWRhZjQ5M2U4N2JhNzZhYjJiOWVmNzZhLnNldENvbnRlbnQoaHRtbF85MzkzODdkZTFlZjU0M2Q2YjVkY2ZkM2EzMGRkMDFmNik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9kZWY2ZDQxNDkzNzc0ZmFhYjMzNjYyMmM4NTIzYmQwYS5iaW5kUG9wdXAocG9wdXBfNGVhM2ZmOTQ1ZGFmNDkzZTg3YmE3NmFiMmI5ZWY3NmEpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMTVmZTA3ZTdhYTIxNDM2ZjllNTI1MWY1MTMzYmU5MTUgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDY0MzUyLC03OS4zNzQ4NDU5OTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8wN2NhYjRhZGYyMTA0NDBiYjhhNGEzZjUxNTIxYzcwYSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF83M2QwY2Y2MTQ2Nzc0NWQ3OTk4Yjg4NDAzNmU3Nzc2YyA9ICQoJzxkaXYgaWQ9Imh0bWxfNzNkMGNmNjE0Njc3NDVkNzk5OGI4ODQwMzZlNzc3NmMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlN0biBBIFBPIEJveGVzIDI1IFRoZSBFc3BsYW5hZGUsIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzA3Y2FiNGFkZjIxMDQ0MGJiOGE0YTNmNTE1MjFjNzBhLnNldENvbnRlbnQoaHRtbF83M2QwY2Y2MTQ2Nzc0NWQ3OTk4Yjg4NDAzNmU3Nzc2Yyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8xNWZlMDdlN2FhMjE0MzZmOWU1MjUxZjUxMzNiZTkxNS5iaW5kUG9wdXAocG9wdXBfMDdjYWI0YWRmMjEwNDQwYmI4YTRhM2Y1MTUyMWM3MGEpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNmE4OGRkZGY2MDExNDc3MDk4YjM2ZDdiY2NkMDYzYmYgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDg0MjkyLC03OS4zODIyODAyXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2U4ZGIyZjY5MTg0MjQwNDM4OTY3NTA1ZTc4OTlhODcyID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzMwZTlhZGFkNDk2ZjQ4ZjE5OTZmNzdlYzQ5NGJkZmNkID0gJCgnPGRpdiBpZD0iaHRtbF8zMGU5YWRhZDQ5NmY0OGYxOTk2Zjc3ZWM0OTRiZGZjZCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Rmlyc3QgQ2FuYWRpYW4gUGxhY2UsIFVuZGVyZ3JvdW5kIGNpdHksIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2U4ZGIyZjY5MTg0MjQwNDM4OTY3NTA1ZTc4OTlhODcyLnNldENvbnRlbnQoaHRtbF8zMGU5YWRhZDQ5NmY0OGYxOTk2Zjc3ZWM0OTRiZGZjZCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl82YTg4ZGRkZjYwMTE0NzcwOThiMzZkN2JjY2QwNjNiZi5iaW5kUG9wdXAocG9wdXBfZThkYjJmNjkxODQyNDA0Mzg5Njc1MDVlNzg5OWE4NzIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOWJhNGU0YzgxMjY0NDI0Y2JjNDYzYzk0NzMzMWE1NjggPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MTg1MTc5OTk5OTk5OTYsLTc5LjQ2NDc2MzI5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzIyZDNhNmNmOWU5OTQ1Y2ZhOTkxNTkxN2NhMGZmMDk0ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzI2Y2QyNmM4MmYxZDQ4ZDg5OGE2OWIwMjliN2JiNzU5ID0gJCgnPGRpdiBpZD0iaHRtbF8yNmNkMjZjODJmMWQ0OGQ4OThhNjliMDI5YjdiYjc1OSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TGF3cmVuY2UgSGVpZ2h0cywgTGF3cmVuY2UgTWFub3IsIE5vcnRoIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzIyZDNhNmNmOWU5OTQ1Y2ZhOTkxNTkxN2NhMGZmMDk0LnNldENvbnRlbnQoaHRtbF8yNmNkMjZjODJmMWQ0OGQ4OThhNjliMDI5YjdiYjc1OSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl85YmE0ZTRjODEyNjQ0MjRjYmM0NjNjOTQ3MzMxYTU2OC5iaW5kUG9wdXAocG9wdXBfMjJkM2E2Y2Y5ZTk5NDVjZmE5OTE1OTE3Y2EwZmYwOTQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfZTk5NmQxMmMxZmM4NGIzODgyNjllM2I1MDhmYmRkMzQgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MDk1NzcsLTc5LjQ0NTA3MjU5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzg5ZjNiNmU5OWIzNTRmZTE4M2M4MGZkMDc3ZGQ4NGQxID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzE4NzM3NTg4ODIxMjQ4YjBhMGYzN2U0ZTM4YTc1YTg3ID0gJCgnPGRpdiBpZD0iaHRtbF8xODczNzU4ODgyMTI0OGIwYTBmMzdlNGUzOGE3NWE4NyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+R2xlbmNhaXJuLCBOb3J0aCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF84OWYzYjZlOTliMzU0ZmUxODNjODBmZDA3N2RkODRkMS5zZXRDb250ZW50KGh0bWxfMTg3Mzc1ODg4MjEyNDhiMGEwZjM3ZTRlMzhhNzVhODcpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfZTk5NmQxMmMxZmM4NGIzODgyNjllM2I1MDhmYmRkMzQuYmluZFBvcHVwKHBvcHVwXzg5ZjNiNmU5OWIzNTRmZTE4M2M4MGZkMDc3ZGQ4NGQxKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzg0MjBhZWRmZGY1ODQ5Y2RiNGM2NmEwMjA3ZTJhZWE2ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjkzNzgxMywtNzkuNDI4MTkxNDAwMDAwMDJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMDI4Y2IxNTI0ZWU1NDZlNmJkMGQ0N2QzYjVmZmJmNDIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNzgxMTY4OWIyNWMyNGY0Y2E4ZDFiZDZiMTk1OWNmYTcgPSAkKCc8ZGl2IGlkPSJodG1sXzc4MTE2ODliMjVjMjRmNGNhOGQxYmQ2YjE5NTljZmE3IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5IdW1ld29vZC1DZWRhcnZhbGUsIFlvcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzAyOGNiMTUyNGVlNTQ2ZTZiZDBkNDdkM2I1ZmZiZjQyLnNldENvbnRlbnQoaHRtbF83ODExNjg5YjI1YzI0ZjRjYThkMWJkNmIxOTU5Y2ZhNyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl84NDIwYWVkZmRmNTg0OWNkYjRjNjZhMDIwN2UyYWVhNi5iaW5kUG9wdXAocG9wdXBfMDI4Y2IxNTI0ZWU1NDZlNmJkMGQ0N2QzYjVmZmJmNDIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfY2UxNzQ5MWIwNDMxNDE4MGFhMGMzNWJhNjYzNWNmOTQgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42ODkwMjU2LC03OS40NTM1MTJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfY2E1NDlhOTI3ZGYzNGQyMmJlMDM5NzU2NzU0ZjlkNmIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfZGIxMTc3NDUyMTc5NDFmY2E4ZWFmNzdkNmM1YTMyNWMgPSAkKCc8ZGl2IGlkPSJodG1sX2RiMTE3NzQ1MjE3OTQxZmNhOGVhZjc3ZDZjNWEzMjVjIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5DYWxlZG9uaWEtRmFpcmJhbmtzLCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9jYTU0OWE5MjdkZjM0ZDIyYmUwMzk3NTY3NTRmOWQ2Yi5zZXRDb250ZW50KGh0bWxfZGIxMTc3NDUyMTc5NDFmY2E4ZWFmNzdkNmM1YTMyNWMpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfY2UxNzQ5MWIwNDMxNDE4MGFhMGMzNWJhNjYzNWNmOTQuYmluZFBvcHVwKHBvcHVwX2NhNTQ5YTkyN2RmMzRkMjJiZTAzOTc1Njc1NGY5ZDZiKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzM1NThmNDA3Mzc3NjQ3ZTFiNGY3NzMxNTIzYTkzNTQwID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjY5NTQyLC03OS40MjI1NjM3XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2JlMGE2YjY4ZjIxMjQ4Yzc4ZmJlMDU1MmM2ZmIwYTFkID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzczNjM2Mjk0ZWM4ZDQ5Y2Y5ZTA3NzUwZmRlZWQ3YTQxID0gJCgnPGRpdiBpZD0iaHRtbF83MzYzNjI5NGVjOGQ0OWNmOWUwNzc1MGZkZWVkN2E0MSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Q2hyaXN0aWUsIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2JlMGE2YjY4ZjIxMjQ4Yzc4ZmJlMDU1MmM2ZmIwYTFkLnNldENvbnRlbnQoaHRtbF83MzYzNjI5NGVjOGQ0OWNmOWUwNzc1MGZkZWVkN2E0MSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8zNTU4ZjQwNzM3NzY0N2UxYjRmNzczMTUyM2E5MzU0MC5iaW5kUG9wdXAocG9wdXBfYmUwYTZiNjhmMjEyNDhjNzhmYmUwNTUyYzZmYjBhMWQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYzMyZDI4ZGZlMTA1NDVlMmFiZWU5MDAwNjhlOTAxNWEgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NjkwMDUxMDAwMDAwMSwtNzkuNDQyMjU5M10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8xMDJjNDJmZTY0YzA0ZjZhODA5ZjFkOGQyYjY0ZTNmZCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9kMGUwNDkyYzgzMGY0MDAwYjVjZDMzZWVhOTUwYTdlMCA9ICQoJzxkaXYgaWQ9Imh0bWxfZDBlMDQ5MmM4MzBmNDAwMGI1Y2QzM2VlYTk1MGE3ZTAiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkRvdmVyY291cnQgVmlsbGFnZSwgRHVmZmVyaW4sIFdlc3QgVG9yb250bzwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMTAyYzQyZmU2NGMwNGY2YTgwOWYxZDhkMmI2NGUzZmQuc2V0Q29udGVudChodG1sX2QwZTA0OTJjODMwZjQwMDBiNWNkMzNlZWE5NTBhN2UwKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2MzMmQyOGRmZTEwNTQ1ZTJhYmVlOTAwMDY4ZTkwMTVhLmJpbmRQb3B1cChwb3B1cF8xMDJjNDJmZTY0YzA0ZjZhODA5ZjFkOGQyYjY0ZTNmZCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9kMTMwZGU5NTc5YzE0MGY2OWU1OGMzNjhhOTQ3ZDdlMSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY0NzkyNjcwMDAwMDAwNiwtNzkuNDE5NzQ5N10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF84M2E4NmZkNmVjYTU0Zjg2YjE5YjkwZDViOWE1ZDZmNyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9jMDVjYTc2MzM3N2M0MTc2YmRmNWQ0NWE0ZWIzZWQzZCA9ICQoJzxkaXYgaWQ9Imh0bWxfYzA1Y2E3NjMzNzdjNDE3NmJkZjVkNDVhNGViM2VkM2QiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkxpdHRsZSBQb3J0dWdhbCwgVHJpbml0eSwgV2VzdCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF84M2E4NmZkNmVjYTU0Zjg2YjE5YjkwZDViOWE1ZDZmNy5zZXRDb250ZW50KGh0bWxfYzA1Y2E3NjMzNzdjNDE3NmJkZjVkNDVhNGViM2VkM2QpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfZDEzMGRlOTU3OWMxNDBmNjllNThjMzY4YTk0N2Q3ZTEuYmluZFBvcHVwKHBvcHVwXzgzYTg2ZmQ2ZWNhNTRmODZiMTliOTBkNWI5YTVkNmY3KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzVhNDFiMmVmMjA5OTRmOTY5YmNlMTk4MzQ0OWViN2I5ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjM2ODQ3MiwtNzkuNDI4MTkxNDAwMDAwMDJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMDliMmQ5NjgwODY0NDdkMThmMzVkY2VlZTk2YzdmZDAgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYzcyYzMzYTUyMTVlNDViYjg0MWUzMDNjOTA0MTY2ZDIgPSAkKCc8ZGl2IGlkPSJodG1sX2M3MmMzM2E1MjE1ZTQ1YmI4NDFlMzAzYzkwNDE2NmQyIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Ccm9ja3RvbiwgRXhoaWJpdGlvbiBQbGFjZSwgUGFya2RhbGUgVmlsbGFnZSwgV2VzdCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8wOWIyZDk2ODA4NjQ0N2QxOGYzNWRjZWVlOTZjN2ZkMC5zZXRDb250ZW50KGh0bWxfYzcyYzMzYTUyMTVlNDViYjg0MWUzMDNjOTA0MTY2ZDIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNWE0MWIyZWYyMDk5NGY5NjliY2UxOTgzNDQ5ZWI3YjkuYmluZFBvcHVwKHBvcHVwXzA5YjJkOTY4MDg2NDQ3ZDE4ZjM1ZGNlZWU5NmM3ZmQwKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2Y0MjBiZWVkNGI5MjQzOGU5ZmIwOTI1OGZjNWRmZjdlID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzEzNzU2MjAwMDAwMDA2LC03OS40OTAwNzM4XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2Q5OGI2OWY4MDk5YzQ0NzY4MGQ5YWJjMjAyOGY4ODMyID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzY2OWVkNGZiMDI2NDRjMjM5YTUxOTI5ODk1ZmJjZWY4ID0gJCgnPGRpdiBpZD0iaHRtbF82NjllZDRmYjAyNjQ0YzIzOWE1MTkyOTg5NWZiY2VmOCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RG93bnN2aWV3LCBOb3J0aCBQYXJrLCBVcHdvb2QgUGFyaywgTm9ydGggWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZDk4YjY5ZjgwOTljNDQ3NjgwZDlhYmMyMDI4Zjg4MzIuc2V0Q29udGVudChodG1sXzY2OWVkNGZiMDI2NDRjMjM5YTUxOTI5ODk1ZmJjZWY4KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2Y0MjBiZWVkNGI5MjQzOGU5ZmIwOTI1OGZjNWRmZjdlLmJpbmRQb3B1cChwb3B1cF9kOThiNjlmODA5OWM0NDc2ODBkOWFiYzIwMjhmODgzMik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9iZDhmYzg1NzhlMjk0NTU3YjRmZjlhNDY1OGZjNWQxOCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY5MTExNTgsLTc5LjQ3NjAxMzI5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2IxNjE2YjBlMTUzYzQ4ZDc4ZTExNmU0MWUyMjhkYTZlID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2E3ZmU5M2YwYTQyMjQzMjRiZjE5NWE1MzM0OGY1MDBmID0gJCgnPGRpdiBpZD0iaHRtbF9hN2ZlOTNmMGE0MjI0MzI0YmYxOTVhNTMzNDhmNTAwZiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RGVsIFJheSwgS2VlbGVzZGFsZSwgTW91bnQgRGVubmlzLCBTaWx2ZXJ0aG9ybiwgWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfYjE2MTZiMGUxNTNjNDhkNzhlMTE2ZTQxZTIyOGRhNmUuc2V0Q29udGVudChodG1sX2E3ZmU5M2YwYTQyMjQzMjRiZjE5NWE1MzM0OGY1MDBmKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2JkOGZjODU3OGUyOTQ1NTdiNGZmOWE0NjU4ZmM1ZDE4LmJpbmRQb3B1cChwb3B1cF9iMTYxNmIwZTE1M2M0OGQ3OGUxMTZlNDFlMjI4ZGE2ZSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl80ZjUzZDlkNmM0M2I0NTY0OWNkNmE3M2VmZGY1MzFhZCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY3MzE4NTI5OTk5OTk5LC03OS40ODcyNjE5MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9mZmE2ZmRlMzEyZmY0M2FlODdkMTY3NzFkNTI0MDc2NiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9lMzY1N2Y0YTIxZmI0NDNiYjg0ZjBlMDAyODIwYjg4NiA9ICQoJzxkaXYgaWQ9Imh0bWxfZTM2NTdmNGEyMWZiNDQzYmI4NGYwZTAwMjgyMGI4ODYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlRoZSBKdW5jdGlvbiBOb3J0aCwgUnVubnltZWRlLCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9mZmE2ZmRlMzEyZmY0M2FlODdkMTY3NzFkNTI0MDc2Ni5zZXRDb250ZW50KGh0bWxfZTM2NTdmNGEyMWZiNDQzYmI4NGYwZTAwMjgyMGI4ODYpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNGY1M2Q5ZDZjNDNiNDU2NDljZDZhNzNlZmRmNTMxYWQuYmluZFBvcHVwKHBvcHVwX2ZmYTZmZGUzMTJmZjQzYWU4N2QxNjc3MWQ1MjQwNzY2KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2E1YTQwMzJiNGM4ZjRmOTJiZjc1YWJlNjA0ZGI4Mjk2ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjYxNjA4MywtNzkuNDY0NzYzMjk5OTk5OTldLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfODYyYjg0YzJiNGVmNDRiNzk5YjdjNDg4ZGYyNWMyZTYgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYWI3ODlkMTNhZWE0NDgzNDkwNzMzNDhhMTNjNjVjNTMgPSAkKCc8ZGl2IGlkPSJodG1sX2FiNzg5ZDEzYWVhNDQ4MzQ5MDczMzQ4YTEzYzY1YzUzIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5IaWdoIFBhcmssIFRoZSBKdW5jdGlvbiBTb3V0aCwgV2VzdCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF84NjJiODRjMmI0ZWY0NGI3OTliN2M0ODhkZjI1YzJlNi5zZXRDb250ZW50KGh0bWxfYWI3ODlkMTNhZWE0NDgzNDkwNzMzNDhhMTNjNjVjNTMpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYTVhNDAzMmI0YzhmNGY5MmJmNzVhYmU2MDRkYjgyOTYuYmluZFBvcHVwKHBvcHVwXzg2MmI4NGMyYjRlZjQ0Yjc5OWI3YzQ4OGRmMjVjMmU2KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzkyNmM2MmE4ZDY2NTQzNDJhMWIwYmM5ZmUxYWRiZDQ2ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjQ4OTU5NywtNzkuNDU2MzI1XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzI3ZDhhZWMwOWQzOTQzYWJhOTkzNGJhMDQzZDA1MWE0ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2IyMDRjMDg4YzUzMzRlNDZiNjQwYjFlZWViZGExYTJjID0gJCgnPGRpdiBpZD0iaHRtbF9iMjA0YzA4OGM1MzM0ZTQ2YjY0MGIxZWVlYmRhMWEyYyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+UGFya2RhbGUsIFJvbmNlc3ZhbGxlcywgV2VzdCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8yN2Q4YWVjMDlkMzk0M2FiYTk5MzRiYTA0M2QwNTFhNC5zZXRDb250ZW50KGh0bWxfYjIwNGMwODhjNTMzNGU0NmI2NDBiMWVlZWJkYTFhMmMpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfOTI2YzYyYThkNjY1NDM0MmExYjBiYzlmZTFhZGJkNDYuYmluZFBvcHVwKHBvcHVwXzI3ZDhhZWMwOWQzOTQzYWJhOTkzNGJhMDQzZDA1MWE0KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2M0MWUwZTRjNTY0NTRiOTBhZWEzMzhjYWE4NzRjMzMzID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjUxNTcwNiwtNzkuNDg0NDQ5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9iZDBkZjE1YTcwOTE0ZDI5ODMyYjVlMzQwNzY5MDc3OCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF80YmNlMmVhNWY0YzE0NTlmOTlhODVlZjBmZDY4ZmIxYSA9ICQoJzxkaXYgaWQ9Imh0bWxfNGJjZTJlYTVmNGMxNDU5Zjk5YTg1ZWYwZmQ2OGZiMWEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlJ1bm55bWVkZSwgU3dhbnNlYSwgV2VzdCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9iZDBkZjE1YTcwOTE0ZDI5ODMyYjVlMzQwNzY5MDc3OC5zZXRDb250ZW50KGh0bWxfNGJjZTJlYTVmNGMxNDU5Zjk5YTg1ZWYwZmQ2OGZiMWEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYzQxZTBlNGM1NjQ1NGI5MGFlYTMzOGNhYTg3NGMzMzMuYmluZFBvcHVwKHBvcHVwX2JkMGRmMTVhNzA5MTRkMjk4MzJiNWUzNDA3NjkwNzc4KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzgwYmUwMWJmMDc0YzRlN2ZiMGNmMDg1ODViNDJhMjk2ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjYyMzAxNSwtNzkuMzg5NDkzOF0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9kOGFlNTE3YzZjZjU0Y2JmOTFkMTZiNGNmYzBjODQ4OSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84OTg2N2MyOWM4NmU0ZDY1ODlmNWRmOTZhZTMxZDljMiA9ICQoJzxkaXYgaWQ9Imh0bWxfODk4NjdjMjljODZlNGQ2NTg5ZjVkZjk2YWUzMWQ5YzIiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlF1ZWVuJiMzOTtzIFBhcmssIFF1ZWVuJiMzOTtzIFBhcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2Q4YWU1MTdjNmNmNTRjYmY5MWQxNmI0Y2ZjMGM4NDg5LnNldENvbnRlbnQoaHRtbF84OTg2N2MyOWM4NmU0ZDY1ODlmNWRmOTZhZTMxZDljMik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl84MGJlMDFiZjA3NGM0ZTdmYjBjZjA4NTg1YjQyYTI5Ni5iaW5kUG9wdXAocG9wdXBfZDhhZTUxN2M2Y2Y1NGNiZjkxZDE2YjRjZmMwYzg0ODkpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMTRlOTc4MTQxNmE0NGUyZDk1NDZjZjNkNDM0YWNhNzQgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42MzY5NjU2LC03OS42MTU4MTg5OTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8wN2I1ZWJiODVkMzg0YjNiYTU0OGFiZjQwY2M0NWEzNyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9mZDg1N2UwNzg5ZjE0MzVkYTBkMzczNzNiMDA3YTlmMiA9ICQoJzxkaXYgaWQ9Imh0bWxfZmQ4NTdlMDc4OWYxNDM1ZGEwZDM3MzczYjAwN2E5ZjIiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNhbmFkYSBQb3N0IEdhdGV3YXkgUHJvY2Vzc2luZyBDZW50cmUsIE1pc3Npc3NhdWdhPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8wN2I1ZWJiODVkMzg0YjNiYTU0OGFiZjQwY2M0NWEzNy5zZXRDb250ZW50KGh0bWxfZmQ4NTdlMDc4OWYxNDM1ZGEwZDM3MzczYjAwN2E5ZjIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMTRlOTc4MTQxNmE0NGUyZDk1NDZjZjNkNDM0YWNhNzQuYmluZFBvcHVwKHBvcHVwXzA3YjVlYmI4NWQzODRiM2JhNTQ4YWJmNDBjYzQ1YTM3KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzg3YWVkYmYzZWM4OTQzMDQ4OTA5Zjg3ZmE2ZGNiMjM2ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjYyNzQzOSwtNzkuMzIxNTU4XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzg1ZDQ3NzM3ZjUzZTRlOThhMDllZTNkYmQxMzIwMjUxID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2E2YTE5ZTg4NDEwZjRkZmVhMTVlMGUwOTgzMzViMDA1ID0gJCgnPGRpdiBpZD0iaHRtbF9hNmExOWU4ODQxMGY0ZGZlYTE1ZTBlMDk4MzM1YjAwNSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+QnVzaW5lc3MgUmVwbHkgTWFpbCBQcm9jZXNzaW5nIENlbnRyZSA5NjkgRWFzdGVybiwgRWFzdCBUb3JvbnRvPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF84NWQ0NzczN2Y1M2U0ZTk4YTA5ZWUzZGJkMTMyMDI1MS5zZXRDb250ZW50KGh0bWxfYTZhMTllODg0MTBmNGRmZWExNWUwZTA5ODMzNWIwMDUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfODdhZWRiZjNlYzg5NDMwNDg5MDlmODdmYTZkY2IyMzYuYmluZFBvcHVwKHBvcHVwXzg1ZDQ3NzM3ZjUzZTRlOThhMDllZTNkYmQxMzIwMjUxKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzUyMjYyNWU2ZjcyZjRlY2E4M2M0YzRjODBlYzVlNDZlID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjA1NjQ2NiwtNzkuNTAxMzIwNzAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfNGNiYzU2ZDM5ZjdkNDYzYTg3ODE3NmUyMjBjZTk3MDEgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNzExOTVkMTg2ZTYzNGZkNDkyOTFiNWNlMjc5YzQ3NTYgPSAkKCc8ZGl2IGlkPSJodG1sXzcxMTk1ZDE4NmU2MzRmZDQ5MjkxYjVjZTI3OWM0NzU2IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5IdW1iZXIgQmF5IFNob3JlcywgTWltaWNvIFNvdXRoLCBOZXcgVG9yb250bywgRXRvYmljb2tlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF80Y2JjNTZkMzlmN2Q0NjNhODc4MTc2ZTIyMGNlOTcwMS5zZXRDb250ZW50KGh0bWxfNzExOTVkMTg2ZTYzNGZkNDkyOTFiNWNlMjc5YzQ3NTYpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNTIyNjI1ZTZmNzJmNGVjYTgzYzRjNGM4MGVjNWU0NmUuYmluZFBvcHVwKHBvcHVwXzRjYmM1NmQzOWY3ZDQ2M2E4NzgxNzZlMjIwY2U5NzAxKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzVhNzE5MGQ5NmFlMjQyNTBiMmRjNmY4ZjQzM2I1NzU2ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjAyNDEzNzAwMDAwMDEsLTc5LjU0MzQ4NDA5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzUxZjI5MjUzZWRiODRiNzg5YzI4Nzk4OTExOWQ4NWE5ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2JiYTAwNDI2NmRjNDQzYzBiYTY4MzUxNDczNDIyNjk4ID0gJCgnPGRpdiBpZD0iaHRtbF9iYmEwMDQyNjZkYzQ0M2MwYmE2ODM1MTQ3MzQyMjY5OCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+QWxkZXJ3b29kLCBMb25nIEJyYW5jaCwgRXRvYmljb2tlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF81MWYyOTI1M2VkYjg0Yjc4OWMyODc5ODkxMTlkODVhOS5zZXRDb250ZW50KGh0bWxfYmJhMDA0MjY2ZGM0NDNjMGJhNjgzNTE0NzM0MjI2OTgpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNWE3MTkwZDk2YWUyNDI1MGIyZGM2ZjhmNDMzYjU3NTYuYmluZFBvcHVwKHBvcHVwXzUxZjI5MjUzZWRiODRiNzg5YzI4Nzk4OTExOWQ4NWE5KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzg0NzQ2MjA1ZDQwYTRhOWVhMTk5ZTk2Mjg1ZWE0ZTI0ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjUzNjUzNjAwMDAwMDA1LC03OS41MDY5NDM2XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzY2MmExM2I1YmZhZTRkMjdiODg0MzRlOTQ2OTJkMDNmID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2YxODc1YTUzYzY4NzQ3NTM5MzQzZGJjODg3MzM2NjQ0ID0gJCgnPGRpdiBpZD0iaHRtbF9mMTg3NWE1M2M2ODc0NzUzOTM0M2RiYzg4NzMzNjY0NCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+VGhlIEtpbmdzd2F5LCBNb250Z29tZXJ5IFJvYWQsIE9sZCBNaWxsIE5vcnRoLCBFdG9iaWNva2U8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzY2MmExM2I1YmZhZTRkMjdiODg0MzRlOTQ2OTJkMDNmLnNldENvbnRlbnQoaHRtbF9mMTg3NWE1M2M2ODc0NzUzOTM0M2RiYzg4NzMzNjY0NCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl84NDc0NjIwNWQ0MGE0YTllYTE5OWU5NjI4NWVhNGUyNC5iaW5kUG9wdXAocG9wdXBfNjYyYTEzYjViZmFlNGQyN2I4ODQzNGU5NDY5MmQwM2YpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNDQyZjk1NDBkMjcxNGI5MGE5NTgxMmM0NjBiY2NlYzggPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42MzYyNTc5LC03OS40OTg1MDkwOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9mZmQ1ZDE3MTI0NWI0YTFhYjhjYzc2YmE5MjI4ZWY1YSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9lYmQyN2RmNmM3ZDk0YjA2OTU5NzZiZjgwOTljMmY3NSA9ICQoJzxkaXYgaWQ9Imh0bWxfZWJkMjdkZjZjN2Q5NGIwNjk1OTc2YmY4MDk5YzJmNzUiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkh1bWJlciBCYXksIEtpbmcmIzM5O3MgTWlsbCBQYXJrLCBLaW5nc3dheSBQYXJrIFNvdXRoIEVhc3QsIE1pbWljbyBORSwgT2xkIE1pbGwgU291dGgsIFRoZSBRdWVlbnN3YXkgRWFzdCwgUm95YWwgWW9yayBTb3V0aCBFYXN0LCBTdW5ueWxlYSwgRXRvYmljb2tlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9mZmQ1ZDE3MTI0NWI0YTFhYjhjYzc2YmE5MjI4ZWY1YS5zZXRDb250ZW50KGh0bWxfZWJkMjdkZjZjN2Q5NGIwNjk1OTc2YmY4MDk5YzJmNzUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNDQyZjk1NDBkMjcxNGI5MGE5NTgxMmM0NjBiY2NlYzguYmluZFBvcHVwKHBvcHVwX2ZmZDVkMTcxMjQ1YjRhMWFiOGNjNzZiYTkyMjhlZjVhKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzk0YjE5OGJiMmNmNTRkZjE5MjBhZjU1YWYwNzNlMzUxID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjI4ODQwOCwtNzkuNTIwOTk5NDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfODFkNTcyMDg2YWNkNDE4Zjk4OGZhMGQyZjI0Njk3OWEgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfZTkzOTkxNjcxMDE1NDVlZGJlMjI5ZWQxM2QzNTNiZDQgPSAkKCc8ZGl2IGlkPSJodG1sX2U5Mzk5MTY3MTAxNTQ1ZWRiZTIyOWVkMTNkMzUzYmQ0IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5LaW5nc3dheSBQYXJrIFNvdXRoIFdlc3QsIE1pbWljbyBOVywgVGhlIFF1ZWVuc3dheSBXZXN0LCBSb3lhbCBZb3JrIFNvdXRoIFdlc3QsIFNvdXRoIG9mIEJsb29yLCBFdG9iaWNva2U8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzgxZDU3MjA4NmFjZDQxOGY5ODhmYTBkMmYyNDY5NzlhLnNldENvbnRlbnQoaHRtbF9lOTM5OTE2NzEwMTU0NWVkYmUyMjllZDEzZDM1M2JkNCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl85NGIxOThiYjJjZjU0ZGYxOTIwYWY1NWFmMDczZTM1MS5iaW5kUG9wdXAocG9wdXBfODFkNTcyMDg2YWNkNDE4Zjk4OGZhMGQyZjI0Njk3OWEpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMTQ4NTdkMTMzMDU5NDk2NDk3ZmJiODllMzQxZjg3ZWIgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42Njc4NTU2LC03OS41MzIyNDI0MDAwMDAwMl0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9jNTYyZjQxMjRlNzk0OGE2OGNmNTUzNzg4MjIwNWVlYSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9mMzM0MWM0YzkyNGU0ZTAzYmFkMGQ5MDkyNDBkNDBhZiA9ICQoJzxkaXYgaWQ9Imh0bWxfZjMzNDFjNGM5MjRlNGUwM2JhZDBkOTA5MjQwZDQwYWYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlF1ZWVuJiMzOTtzIFBhcmssIERvd250b3duIFRvcm9udG88L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2M1NjJmNDEyNGU3OTQ4YTY4Y2Y1NTM3ODgyMjA1ZWVhLnNldENvbnRlbnQoaHRtbF9mMzM0MWM0YzkyNGU0ZTAzYmFkMGQ5MDkyNDBkNDBhZik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8xNDg1N2QxMzMwNTk0OTY0OTdmYmI4OWUzNDFmODdlYi5iaW5kUG9wdXAocG9wdXBfYzU2MmY0MTI0ZTc5NDhhNjhjZjU1Mzc4ODIyMDVlZWEpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMzAzZGZjZmZmMWIyNDFkZGFlYTY0ODdmNWU0ZGJjZWYgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NTA5NDMyLC03OS41NTQ3MjQ0MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF82OWE1ZWQ2MDYzYWY0NzE5OThhOTNjNzU2MjAyNjdmOSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9mNjE2ZWVhZDg4MWI0OTRmODFiN2Q1MTMyZWNkN2NlZCA9ICQoJzxkaXYgaWQ9Imh0bWxfZjYxNmVlYWQ4ODFiNDk0ZjgxYjdkNTEzMmVjZDdjZWQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNsb3ZlcmRhbGUsIElzbGluZ3RvbiwgTWFydGluIEdyb3ZlLCBQcmluY2VzcyBHYXJkZW5zLCBXZXN0IERlYW5lIFBhcmssIEV0b2JpY29rZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNjlhNWVkNjA2M2FmNDcxOTk4YTkzYzc1NjIwMjY3Zjkuc2V0Q29udGVudChodG1sX2Y2MTZlZWFkODgxYjQ5NGY4MWI3ZDUxMzJlY2Q3Y2VkKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzMwM2RmY2ZmZjFiMjQxZGRhZWE2NDg3ZjVlNGRiY2VmLmJpbmRQb3B1cChwb3B1cF82OWE1ZWQ2MDYzYWY0NzE5OThhOTNjNzU2MjAyNjdmOSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9mNWU0NDQ0OTY2ZTc0OWE0OGMxZWYwZTliOTBkOTUyMCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY0MzUxNTIsLTc5LjU3NzIwMDc5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzY2ZDRiODNmZDdjMjQwYjA4NjhlMjRhODU4M2MzZjRkID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzY4M2I1MmI3MDgyMzQ1MTliOGJlYmQ1ODg2MWI0NjgwID0gJCgnPGRpdiBpZD0iaHRtbF82ODNiNTJiNzA4MjM0NTE5YjhiZWJkNTg4NjFiNDY4MCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Qmxvb3JkYWxlIEdhcmRlbnMsIEVyaW5nYXRlLCBNYXJrbGFuZCBXb29kLCBPbGQgQnVybmhhbXRob3JwZSwgRXRvYmljb2tlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF82NmQ0YjgzZmQ3YzI0MGIwODY4ZTI0YTg1ODNjM2Y0ZC5zZXRDb250ZW50KGh0bWxfNjgzYjUyYjcwODIzNDUxOWI4YmViZDU4ODYxYjQ2ODApOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfZjVlNDQ0NDk2NmU3NDlhNDhjMWVmMGU5YjkwZDk1MjAuYmluZFBvcHVwKHBvcHVwXzY2ZDRiODNmZDdjMjQwYjA4NjhlMjRhODU4M2MzZjRkKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2VhMWJhZGI2Y2JmNjRjODhhZWMzZDgxYzhlNmQwMjRjID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzU2MzAzMywtNzkuNTY1OTYzMjk5OTk5OTldLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYWM5NGNhYzViMmE1NDhjN2JkODZlOTY4MzFjOTY4ODEgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfZTc4MzVkMWE0MDFmNDkyNmFkNGE2OTRiMjlhM2Y5MGMgPSAkKCc8ZGl2IGlkPSJodG1sX2U3ODM1ZDFhNDAxZjQ5MjZhZDRhNjk0YjI5YTNmOTBjIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5IdW1iZXIgU3VtbWl0LCBOb3J0aCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9hYzk0Y2FjNWIyYTU0OGM3YmQ4NmU5NjgzMWM5Njg4MS5zZXRDb250ZW50KGh0bWxfZTc4MzVkMWE0MDFmNDkyNmFkNGE2OTRiMjlhM2Y5MGMpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfZWExYmFkYjZjYmY2NGM4OGFlYzNkODFjOGU2ZDAyNGMuYmluZFBvcHVwKHBvcHVwX2FjOTRjYWM1YjJhNTQ4YzdiZDg2ZTk2ODMxYzk2ODgxKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzljZmJjMmE4ZGY4NjQyNDhhMDBiOTdhMjhiMWYyOTZlID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzI0NzY1OSwtNzkuNTMyMjQyNDAwMDAwMDJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYmIyNTkzYTUxMWY5NGE3ZmIyNTk1ODFjZmUzZjZhZjAgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfZTk1OTY3ODg1ZmRkNDIzYWFmNWU0NDcwZjdhMTE1YzEgPSAkKCc8ZGl2IGlkPSJodG1sX2U5NTk2Nzg4NWZkZDQyM2FhZjVlNDQ3MGY3YTExNWMxIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5FbWVyeSwgSHVtYmVybGVhLCBOb3J0aCBZb3JrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9iYjI1OTNhNTExZjk0YTdmYjI1OTU4MWNmZTNmNmFmMC5zZXRDb250ZW50KGh0bWxfZTk1OTY3ODg1ZmRkNDIzYWFmNWU0NDcwZjdhMTE1YzEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfOWNmYmMyYThkZjg2NDI0OGEwMGI5N2EyOGIxZjI5NmUuYmluZFBvcHVwKHBvcHVwX2JiMjU5M2E1MTFmOTRhN2ZiMjU5NTgxY2ZlM2Y2YWYwKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzc2ZDE4OGY2ZTk3ZjRmYjk5Mjg3NThkMmNmMzMwNDc5ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzA2ODc2LC03OS41MTgxODg0MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8yZTJjNWIxNThkNzk0ZTU0OGJiMTNlYWVkMzlmNWE0YyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9jZDJkNDdmZTA3YTI0YzM3OTg3MTg0ZGQzMTQwMWU5MyA9ICQoJzxkaXYgaWQ9Imh0bWxfY2QyZDQ3ZmUwN2EyNGMzNzk4NzE4NGRkMzE0MDFlOTMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPldlc3RvbiwgWW9yazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMmUyYzViMTU4ZDc5NGU1NDhiYjEzZWFlZDM5ZjVhNGMuc2V0Q29udGVudChodG1sX2NkMmQ0N2ZlMDdhMjRjMzc5ODcxODRkZDMxNDAxZTkzKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzc2ZDE4OGY2ZTk3ZjRmYjk5Mjg3NThkMmNmMzMwNDc5LmJpbmRQb3B1cChwb3B1cF8yZTJjNWIxNThkNzk0ZTU0OGJiMTNlYWVkMzlmNWE0Yyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8xZjI5NmUwMzI5ZjM0OTk4YTkyZjU4MzliZGNjODIyYSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY5NjMxOSwtNzkuNTMyMjQyNDAwMDAwMDJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZmZhYTYwNmM1ZTA3NGRhY2E2YTFkOTgzN2MyNWJkZTMpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfOTdkZjQ1ODg0ODNiNDhmYTlkYzhkNWQ3ZjQ0NzQzZmIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYzk1OTgxMmZjNzk3NGU0ZGFmZDZkZWQzMzk4ZmQ2NTQgPSAkKCc8ZGl2IGlkPSJodG1sX2M5NTk4MTJmYzc5NzRlNGRhZmQ2ZGVkMzM5OGZkNjU0IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5XZXN0bW91bnQsIEV0b2JpY29rZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfOTdkZjQ1ODg0ODNiNDhmYTlkYzhkNWQ3ZjQ0NzQzZmIuc2V0Q29udGVudChodG1sX2M5NTk4MTJmYzc5NzRlNGRhZmQ2ZGVkMzM5OGZkNjU0KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzFmMjk2ZTAzMjlmMzQ5OThhOTJmNTgzOWJkY2M4MjJhLmJpbmRQb3B1cChwb3B1cF85N2RmNDU4ODQ4M2I0OGZhOWRjOGQ1ZDdmNDQ3NDNmYik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl81NzIyNDUyYWNmZGM0Mzk4ODliYWUxNzIyM2ExNWU1MyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY4ODkwNTQsLTc5LjU1NDcyNDQwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2ZmYWE2MDZjNWUwNzRkYWNhNmExZDk4MzdjMjViZGUzKTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzI3MDAwYTc3ODEyMDQxYTc5OWYzNDY2ZDY1ZjVmYjQwID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2Q4MWZhNzVlMGU3NjQzMTY5MTcxODA5NjYwMDU0YTlmID0gJCgnPGRpdiBpZD0iaHRtbF9kODFmYTc1ZTBlNzY0MzE2OTE3MTgwOTY2MDA1NGE5ZiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+S2luZ3N2aWV3IFZpbGxhZ2UsIE1hcnRpbiBHcm92ZSBHYXJkZW5zLCBSaWNodmlldyBHYXJkZW5zLCBTdC4gUGhpbGxpcHMsIEV0b2JpY29rZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMjcwMDBhNzc4MTIwNDFhNzk5ZjM0NjZkNjVmNWZiNDAuc2V0Q29udGVudChodG1sX2Q4MWZhNzVlMGU3NjQzMTY5MTcxODA5NjYwMDU0YTlmKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzU3MjI0NTJhY2ZkYzQzOTg4OWJhZTE3MjIzYTE1ZTUzLmJpbmRQb3B1cChwb3B1cF8yNzAwMGE3NzgxMjA0MWE3OTlmMzQ2NmQ2NWY1ZmI0MCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl84MTU2OWE3ODUwMDU0NjM4OGMyYzdmNDAwNTBhMzBjNSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjczOTQxNjM5OTk5OTk5NiwtNzkuNTg4NDM2OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9mZGQzNjQwNTJlMGE0OTJhYmUxYmUxZmFmNTFhNTM0NCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9hYWJhNzdjZDNmOWI0Y2M5YjhkMmEyY2ZjMjA3YWQ0NCA9ICQoJzxkaXYgaWQ9Imh0bWxfYWFiYTc3Y2QzZjliNGNjOWI4ZDJhMmNmYzIwN2FkNDQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkFsYmlvbiBHYXJkZW5zLCBCZWF1bW9uZCBIZWlnaHRzLCBIdW1iZXJnYXRlLCBKYW1lc3Rvd24sIE1vdW50IE9saXZlLCBTaWx2ZXJzdG9uZSwgU291dGggU3RlZWxlcywgVGhpc3RsZXRvd24sIEV0b2JpY29rZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZmRkMzY0MDUyZTBhNDkyYWJlMWJlMWZhZjUxYTUzNDQuc2V0Q29udGVudChodG1sX2FhYmE3N2NkM2Y5YjRjYzliOGQyYTJjZmMyMDdhZDQ0KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzgxNTY5YTc4NTAwNTQ2Mzg4YzJjN2Y0MDA1MGEzMGM1LmJpbmRQb3B1cChwb3B1cF9mZGQzNjQwNTJlMGE0OTJhYmUxYmUxZmFmNTFhNTM0NCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8xYzYyNzkzZmE1YzQ0ZGZjYTg5OGE4YTg0NzI0MzAyZCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcwNjc0ODI5OTk5OTk5NCwtNzkuNTk0MDU0NF0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9mZmFhNjA2YzVlMDc0ZGFjYTZhMWQ5ODM3YzI1YmRlMyk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF83NzU4ZmQwNDNkNTM0MzgyOTk2NTNhZmMyMjY0ZmYwMiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8yZjgyMjQyZTAyYTg0ZGEzYjQ5NDk5OGM5ZDdkNGM2YSA9ICQoJzxkaXYgaWQ9Imh0bWxfMmY4MjI0MmUwMmE4NGRhM2I0OTQ5OThjOWQ3ZDRjNmEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk5vcnRod2VzdCwgRXRvYmljb2tlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF83NzU4ZmQwNDNkNTM0MzgyOTk2NTNhZmMyMjY0ZmYwMi5zZXRDb250ZW50KGh0bWxfMmY4MjI0MmUwMmE4NGRhM2I0OTQ5OThjOWQ3ZDRjNmEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMWM2Mjc5M2ZhNWM0NGRmY2E4OThhOGE4NDcyNDMwMmQuYmluZFBvcHVwKHBvcHVwXzc3NThmZDA0M2Q1MzQzODI5OTY1M2FmYzIyNjRmZjAyKTsKCiAgICAgICAgICAgIAogICAgICAgIAo8L3NjcmlwdD4=" style="position:absolute;width:100%;height:100%;left:0;top:0;border:none !important;" allowfullscreen webkitallowfullscreen mozallowfullscreen></iframe></div></div>




```python

```


```python

```
