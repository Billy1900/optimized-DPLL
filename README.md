# optimized-DPLL

the optimizetion of DPLL 
===

基本算法思想来源于DPLL算法，对于变元策略进行了改进。具体可以参考https://github.com/Billy1900/DPLL-Algorithm
==

DPLL算法思想如下：

Status DPLL( S) {

/* S为公式对应的子句集。若其满足，返回TURE；否则返回FALSE. */

while(S中存在单子句) { 

在S中选一个单子句L，并将单子句装入结果数组，value置为1；

依据单子句规则，利用L化简S；

if S = Φ return(TRUE);

else if (S中有空子句 ) return（FALSE）；

}

对子句集中的所有变元出现次数进行排序，出现次数最多的选为最终的变元choose（次数统计规则--例：1和-1表示变元1出现了2次）

V = choose;

if DPLL（S ∪v ）return(TURE);

return DPLL(S ∪¬v);

}

说明：优化算法相比DPLL算法 来讲，在选取变元策略上进行了优化。其余算法流程基本保持不变。


１）读取文件的路径在CreateClause函数中被写死，在文件的第５８行，可以在此修改。

２）ｍａｉｎ函数中将文件名写死，在程序文件的第２９３行，可以在此做修改。
