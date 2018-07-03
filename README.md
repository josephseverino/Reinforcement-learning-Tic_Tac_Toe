# Reinforcement-learning-Tic_Tac_Toe

### Introduction
<span style="font-family:Papyrus"> Tic-tac-toe was a classic game I use to play back in my adolescent years. During that time, my friends and I would find ourselves quite unengaged often and so we clung to games like Tic-Tac-Toe to alleviate our boredom. We all claimed to have the dominate strategy to win. However, we soon figured out that once both players were privy to the game, the only player to guarantee a win or tie was the starting player. This advantage only ended in a win if the other player was unable to look-ahead and see the most advantagous moves. However, being the second player only guarantees a tie or loss, unless the other player makes a really bad move. After many iterations of playing, most reasonable players only ended in a tie.
</span>

### Is There a Dominate Strategy?
<span style="font-family:Papyrus"> In this project I explored dynamic progamming in the game of Tic-Tac-Toe. My hypothesis of this experiment was to see if I could get the agent (algorythm that calculates the value function based off epsilon and alpha) to converge on my technique to play the game. Below you see the theory behind why strategy. But first lets discuss my strategy. After doing research and recollecting back to my former years, I concluded starting in the corner was the most advantagous. However, you soon find out that no strategy is dominate unless you reward the agent for acheiving it in fewer steps or find some other unusual way to cohoerce it. In this particular code there is nothing rewarding it for finding it faster. Also, there is nothing in the code to reward ties to be greater than losses. This could change the results. In the case of of starting in the corner, I assumed this was the most dominate strategy becasue probabilistically there were far more permutations that lead to the quickest wins using a trap method. This assumption was good with respect to psychology of playing another person since that other person may not be able to look-ahead and see all possible outcomes earlier in the game. Alternatively, it is just as easy for a computer to look-ahead early as it is later on in the game. Thus, there is no advantage to winner earlier on. Bescause of this, the agent doesn't care if it randomly finds a winning starting move in the corner, in the middle or seldomly on the side. One interesting finding is that it seldomly started in the corner. This is most likely due to being less permutations of winning moves starting in the corner. My below logic may explain that.  
</span>
<p align="center">
  <h3>Tic-Tac-Toe Theory And Probability </>
  <img src="tic-tac-toe.png" )
</p>

### A Brief Theory
<span style="font-family:Papyrus"> In the above diagram, you can see the grid is symmetric in nature, so it is ok to generalize equivilant states to be valued the same in the perfect world. As you will see shortly, this is not the case for this agent or at least it was not what I observed form my many experiments. The next important thing is notice that in the corner case there are 4 out of 5 (one not being showed: the center defensive move) that lead to a win right away if taken advantage of. There are only 1 out of 2 generalized ways to get to a win as fast from starting in middle. However, the middle has many ways further in the future to achieve a win. This is true for the corner start as well but far less of those exist. 
</span>

### Lets See The Agent Play My Stategy


```python
if __name__ == '__main__':
  # train the agent
  p1 = Agent(eps = .1, alpha = .1)
  p2 = Agent(eps = .25, alpha = .1)

```

<p align="center">
  <h3>Tic-Tac-Toe Theory And Probability </>
  <img src="tic-tac-toe2.png" )
</p>
