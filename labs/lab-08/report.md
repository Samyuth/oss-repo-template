# Lab 08 Report - Testing and Continuous Integration

## Part 1

<img alt="cmake generation" src="images/cmake-gui.png" />

## Part 2

The only mistake that I ran into was the copyright but because I was doing part 3 while working on part 2 but this was easily fixed by reverting back to the original version.

<img alt="dashboard output" src="images/dashboard.png" />

## Part 3

Running with ctest obtains the following output showing a failiure:

<img alt="ctest output" src="images/ctest.png" />

Using ctest -VV we can pinpoint that the error occurs with the year

<img alt="ctest -VV output" src="images/ctestvv.png" />

## Part 4

<img alt="pull request" src="images/cicd.png" />

<img alt="workflow" src="images/workflows.png" />

To fix this one option is simply to allow for greater years so you can change the less than to greater than in CMakeCopyRight.cmake

<img alt="fixed" src="images/fix.png" />

Link to the repo: https://github.com/Samyuth/CMakeTesting

