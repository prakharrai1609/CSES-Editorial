<details open>
	<summary>Editorial</summary>
	<br>
	Let's divide the matrix in 2 halves :
	<br>
	<ul>
		<li>First is the upper triangle , which includes the diogonal</li>
		<li>Second is the lower triangle</li>
	</ul> 
	<br>
	If we consider the upper diagonal (In the upper diagonal , y >= x (x and y are the x and y cordinates)):
	<br>
	<ol>
		<li>All odd y cordinates are squares</li>
		<li>When y is odd , it decreases till the diagonal</li>
			<ul>It decreases by (x - 1) ratio</ul>
		<li>When y is even , it increases till the diagonal</li>
			<ul>It increases as : (y-1) * (y-1) + x --> Basically we are taking the sq. odd y coordinates as reference</ul>
	</ol>

</details>