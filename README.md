# PythonCodeForBiostatistics
Author:MdMortuzaHossain<br>
#TTest between group<br>
import numpy as np<br>
from scipy import stats<br>
group_A = np.array([23, 20, 27, 24, 35, 28, 22, 25, 33, 21])<br>
group_B = np.array([31, 22, 34, 27, 28, 25, 26, 30, 29, 23])<br>
t_stat, p_value = stats.ttest_ind(group_A, group_B)<br>
print(f"T-statistic: {t_stat}, P-value: {p_value}")<br>

#OneWay ANOVA between three treatment<br>
import numpy as np<br>
from scipy import stats<br>
group_A = np.array([23, 20, 27, 24, 35, 28, 22, 25, 33, 21])<br>
group_B = np.array([31, 22, 34, 27, 28, 25, 26, 30, 29, 23])<br>
group_C = np.array([29, 30, 28, 32, 31, 27, 33, 26, 34, 35])<br>
f_stat, p_value = stats.f_oneway(group_A, group_B, group_C)<br>
print(f"F-statistic: {f_stat}, P-value: {p_value}")


#bar diagram<br>
import numpy as np<br>
import pandas as pd<br>
import seaborn as sns<br>
import matplotlib.pyplot as plt<br>
group_A = [23, 20, 27, 24, 35, 28, 22, 25, 33, 21]<br>
group_B = [31, 22, 34, 27, 28, 25, 26, 30, 29, 23]<br>
group_C = [29, 30, 28, 32, 31, 27, 33, 26, 34, 35]<br>
data = pd.DataFrame({<br>
    'score': np.concatenate([group_A, group_B, group_C]),<br>
    'group': ['A'] * len(group_A) + ['B'] * len(group_B) + ['C'] * len(group_C)<br>
})<br>
plt.figure(figsize=(10, 6))<br>
sns.boxplot(x='group', y='score', data=data)<br>
plt.title('Boxplot of Scores by Group')<br>
plt.xlabel('Group')<br>
plt.ylabel('Score')<br>
plt.show()<br><br>
