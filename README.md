# PythonCodeForBiostatistics
Author:MdMortuzaHossain
#TTest between group
import numpy as np
from scipy import stats
group_A = np.array([23, 20, 27, 24, 35, 28, 22, 25, 33, 21])
group_B = np.array([31, 22, 34, 27, 28, 25, 26, 30, 29, 23])

t_stat, p_value = stats.ttest_ind(group_A, group_B)
print(f"T-statistic: {t_stat}, P-value: {p_value}")

#OneWay ANOVA between three treatment
import numpy as np
from scipy import stats
group_A = np.array([23, 20, 27, 24, 35, 28, 22, 25, 33, 21])
group_B = np.array([31, 22, 34, 27, 28, 25, 26, 30, 29, 23])
group_C = np.array([29, 30, 28, 32, 31, 27, 33, 26, 34, 35])
f_stat, p_value = stats.f_oneway(group_A, group_B, group_C)
print(f"F-statistic: {f_stat}, P-value: {p_value}")
