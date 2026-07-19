# d4.m
an attempt to fix a failed assertion during FourDescent

See the details in the bug report [https://github.com/Magma-Maths/Magma/issues/102](https://github.com/Magma-Maths/Magma/issues/102).

Full path: */usr/local/magma/package/Geometry/CrvEll/FourDesc/d4.m*.

Use ```SetVerbose("QuotientFD", 1);``` if you want to see the warning **reduced V[i] size to zero?? (not good, re-run or expect higher than optimal number of 4-coverings)**.

The failing assert is re-written as if-statement. When the if-statement fails, the code finishes the job with the optimal number of the 4-coverings ~16 out of 20 times.

My tries to remove the extra 4-coverings as in ```ThreeDescent``` https://github.com/Magma-Maths/Magma/issues/101 were unsuccessful.

I suspect that sometimes the 2-coverings are generated and filtered in such a way that the number of the 4-coverings is destined to be sub-optimal. In that case, re-run usually helps.
