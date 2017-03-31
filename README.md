# Data Visualization with d3 on Prosper Rating and Income Range
<h3> SUMMARY </h3>
<h4> No significant relationship between Prosper rating and income range</h4>
<p>The visualization analyses data on loans. The data are taken from the peer-to-peer lending marketplace called Prosper. The loans originated from 2009 to 2014 and have two main pieces. The Prosper rating, which provides a measure of loan risk, and estimated return to lenders. Estimated return to lenders are essentially the interest received by lenders after costs and losses. In this case, my main focses are income range and prosper rating and their relationship with estimated return, respectively. I also added the numbers of loans in the graph in the form of <b>bars</b> to show how many loans were borrowed against those variables. </p>

<h3> DESIGN </h3>
<body>
<p>When exploring the data, I thought, 'what information I would want to know if I were to lend money through Prosper.' The answer was obvious, the return. The return would be the median value as well, to avoid any outliers. I am a banker and I know that one big factor in return is the risk of default; in this sense, credit rating is important. However, a good credit rating isn't good enough, income needs to be considered as well. That is why I created two visualizations, one with ProsperRating and another with Income Range. I put Propser Rating on X-axis on Prosper Rating vs Loan Return graph and Income Range on x-axis on Income Range vs Loan Return graph. More importantly, the main piece of information I wanted to draw to the eye was how the median estimated return changes as credit risk decreases. I used line to show the trend. I provided two fitting titles for each plot instead of one big title for two plots so the readers would not be confused about what the title is trying to convey.

I also encoded another piece of information, the spread of expected return. That is why I included 1% and 99% for my code. 99% being the highest estimated return and 1% being the lowest estimated return. Median itself does not tell the whole story, I want to know if I would get big return or losses. The bigger the spread, the more likely the bigger return or losses. 

Lastly, I defaulted both plots on <i>All Years</i> to give the audience a sense of how the data looked liked in general. From there they can dig deeper into how the data vary throughout the years. I included years in my visualizations, so the readers can tell how estimated return change over time, from 2009 to 2014. From that, we can get an idea of how directly related credit rating is to the loan return and how directly related income range is to loan return.</p>

Key stories from the exploration:
<ul>
<li>There should be a direct relationship between credit rating and loan return</li>
<li>There is no significant relationship between income range and loan return and number of loans approved</li> 
<li>Loans to less creditworthy borrowers tend to have a much larger spread (maximum return - minimum return) than loans to more creditworthy borrowers. This makes sense, as it explains the tradeoff you have to make when lending to less creditworthy borrowers. The average estimated return is bigger, but there is a chance for bigger losses.</li>
<li>The spread of loan return are approximately the same for all Income Range. However, the numbers of loans are where they differ. Middle class tend to get more loans approved. This makes sense because they need money for expenses, the higher income people usually do not need to take out loan. The spread of loan return in this case are equivalent because the loans are approved because the borrowers would be able to pay back the loan at a certain level.</li>
<li>The spread of loan returns appears to decline fairly consistently over the years from 2009 to 2014. This may be due to the economic downturn of 2009, when lenders likely had to deal with more defaults, thus decreasing minimum expected returns. At the same time, lenders likely expected to be compensated for these risks with higher interest rates, thus increasing maximum estimated returns. The Income Range visualization further proves my point. We can see that there were minimal to none of loans taken for those who are not employed and/or those with $0 income.</li>
</ul>
<p> I started my exploration of visualization with Tableau first. I downladed the data and imported to Tableau. I tried to explore any interesting relationship between different variables and I discovered some interesting relationship. Risk vs Return was the only thing that caught my interest. The risk are the income range and Prosper Rating in Numeric. My goal for both graphs is to make the graph less busy- turn estimated return to percentage form. Also, since the dataset is huge, I had to clean up the data and perform aggregation so dimple and d3 won't crash.</p>

Income Range vs Return 
<br>![Preview](https://github.com/jtsou/Data-Visualization-with-d3/blob/master/Tableau%20img/Income%20Range%20vs%20return%20with%20prosper%20rating.png)<br>
Prosper Rating vs Return 
<br>![Preview](https://github.com/jtsou/Data-Visualization-with-d3/blob/master/Tableau%20img/ProsperRating%20vs%20Return%20.png)<br>

<p>
I chose a scatterplot for median, minimum, and maximum estimated returns. Viewing these points along a common scale is the best visual encoding to ensure the viewer can differetiate in return across risk categories. Color coding is used to help the reader distinguish between median, minimum, and maximum estimated returns. I included median as lightblue, since this is the focus of the visualization and easier on the eyes to emphasize how returns change as loan risk decreases.
</p>
</body>

<h3> Feedback </h3>
<p>After creating the visualization, I came up with the versions in the BeforeFeedBack folder. (https://github.com/jtsou/Data-Visualization-with-d3/tree/master/DraftBeforeFeedBack), and I received the following feedback from my friends, who has little to none background in data visualization. Those are the audience that would most likely play around with my visualizations, so my friends' feedack is exactly what I wanted to know. The feedback are the follow:
<ul>
<li> The visualization is great but there is a part of it that needs improvement like where the legend is located, 
  when I opened the file for loanrate.html, you can make out the words but the letters are cut-off.
  It would probably be good to reduce the image size for both html files to make it fit. </li>
<li>When looking at Prosper Rating vs. Loan Return, I did not understand what does the x-axises mean.</li>
</ul>

In response to those comments, I decided to add more description next to x-axises. I also adjusted the legend size so the letters won't be cut off. I put the files in here (https://github.com/jtsou/Data-Visualization-with-d3/tree/master/Index_final)
</p>
<h3> Resources </h3>
<ul>
<li>Udacity Discussion Forum </li>
<li>Tableau</li>
<li>Started with the code Udacity course provided, made changes here and there.</li>
<li><a href="http://dimplejs.org/examples_index.html">dimplejs.org</a></li>
<li><a href="jsfiddle.net/ch2187dd/">Fiddle</a></li>
</ul>
