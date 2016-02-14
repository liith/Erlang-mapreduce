# Erlang-mapreduce
Small simulation of mapreduce in Erlang for university


Instructions for execution once in the directory that contains the file:

f().
c(proyecto).
MR = proyecto:master(proyecto:initInfo1(), 3).
MR ! {mapreduce, self(), proyecto:map1(), proyecto:reduce1()}.
flush().
f().
c(proyecto).
MR = proyecto:master(proyecto:initInfo2(), 3).
MR ! {mapreduce, self(), proyecto:map2(), proyecto:reduce2()}.
flush().

This will show first an execution which determines the highest temperature of
each city if it's higher than 28º, and then a second example which
displays the best actor from each film (along with their score),
if the score is equal to or higher than 5.
