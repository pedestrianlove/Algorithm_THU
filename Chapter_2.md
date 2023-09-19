# Chapter 2: Getting Started

## 2.1 Example: Insertion sort
- Input: 一個有$$n$$個數字的序列: $$a_1,a_2,\ldots,a_n$$.
- Output: 一個輸入序列的排列組合(permutation)，使其呈現遞增排序的情形。(ordered) 

每一輸for-loop，選出一個key，將其放至正確的位置。由此方法，逐漸增加已排序元素的數目。 
($$n = 0$$時，是不用移動的，因為目前已排序的只有那一個數字)

### INSERTION-SORT(A, n)
```
for i = 1 to (n-1):
    // 選定key作為我們排序的目標。
    key = A[i]

    // 將A[i]插入已排序的子序列A[0:i-1]。
    
    //// 先記錄已排序的子序列的尾端
    j = i - 1

    //// 將後序的元素都往後移，直到比key大為止。
    while j >= 0 and A[j] > key:
        A[j + 1] = A[j]
        j = j - 1

    //// 插入key在最終的j+1(合適)的位置。
    A[j + 1] = key
```

- Sorted in place: 只需常數個額外的變數，而無需另開一個新陣列。
- Pseudocode我的陣列使用0開始，因為this it how it works.

## 2.2 Analyzing algorithm
一個演算法可能使用到的有下列的資源:
- 記憶體 (Memory)
- 通訊 (Communication)
- 頻寬 (Bandwidth)
- Logic gate
- 空間 (Space)
- ***時間 (time)***
其中時間最為重要，因為很難使用金錢換取。
**但是因為變數太多，我們一律假設演算法使用一個處理器(Processor)跟RAM來執行。**

### 2.2.1 Running time
- Best-case: 通常不會聚焦在Best-case上，因為太少發生了。
- Worst-case: 通常為我們討論的焦點，因為它是執行時間的上界(upper-bound)
- Average-case: 我們通常也不太會管，因為都跟Worst-case差不多慘。
