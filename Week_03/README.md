学习笔记

**递归**
范式递归（java）
// Java
public void recur(int level, int param) { 
  // terminator 
  if (level > MAX_LEVEL) { 
    // process result 
    return; 
  }
  // process current logic 
  process(level, param); 
  // drill down 
  recur( level: level + 1, newParam); 
  // restore current status 

}
<u>*思维要点</u>*：
1.不要人肉进行递归（最大误区）
2.找到最近最简方法，将其拆解成可重复解决的问题（重复子问题）
3.数学归纳法思维

**分治  拆分子任务**
// Java
private static int divide_conquer(Problem problem, ) {

  if (problem == NULL) {
    int res = process_last_result();
    return res;     
  }
  subProblems = split_problem(problem)

  res0 = divide_conquer(subProblems[0])
  res1 = divide_conquer(subProblems[1])

  result = process_result(res0, res1);

  return result;
}

**回溯** 试错的思想 可以取消上一步甚至上几步的计算,再通过其它的可能的分步解答再次尝试寻找问题的答案。 典型的应用 数独，八皇后。