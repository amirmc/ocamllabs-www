---
uid: timada
date: 2017-01-09
enddate: 2017-01-15
week: 3
generator: furore
---

- Network performance evaluation
  - iperf tests for tracing done, so I am summarizing findings from the tests
  - Findings
    - the CPU utilization on the sender side reached 100%
    - there were waiting (or blocking) periods on the sender side, they are not anticipated and occupy 50% of the total network processing time. (Due to thread scheduling?)
    - the waiting periods always occurred during a "ring.write" phase
    - The receiver side had sleeping periods which would correspond to the waiting periods above, so its CPU utilization was not so high.
  - I will need to specify what triggers the waiting periods.

