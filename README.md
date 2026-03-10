<h1>Basic Resource Allocation Project Using Excel</h1>

<h2>Description</h2>
The project involves a job assignment of jobs between 3 people with the objective of maximising efficiency. 
<br />

<h2>Languages and Utilities Used</h2>

- Excel (Spreadsheet Modeling, Linear Programming (LP))
- Manual calculation
<br />

[Project Excel File](https://github.com/jordanbolling/Data-Envelopment-Analysis-DEA-Analysis-Using-Excel/blob/main/DEA%20Excel.xlsx)

#### **Project Workflow**

There are 2 prime methods of solving this problem and when the results of each are compared an optimal result can be identified. These are the Hungarian Algorithm and through a mathematical model. Both are used below.
<br />

**The Hungarian Algorithm**

Out of all the possible graphical methods, this is the best for solving this problem as it is superior for when each activity is done by a different person and the objective is to find the minimum cost to complete all the activities. It follows the below steps.

o	Construction of matrix of the bids by each person for each job.
o	Subtracting the minimum value from each row.
o	Subtracting the minimum value from each column from the new set of values.

<p align="center">
<img src="https://i.ibb.co/hx9cdznb/Screenshot-2026-03-10-at-09-05-56.png"/>
<br/>
</p>

The first 3 steps are done here, and a new set of values have been found.
o	Cover all the zeros with the minimum amount of horizontal and vertical lines.

<p align="center">
<img src="https://i.ibb.co/qLHZjVpx/Screenshot-2026-03-10-at-09-06-08.png"/>
<br/>
</p>

The number of lines used was 3, which is the equal to the dimensions of the matrix (3 by 3). This indicates that the problem is balanced, and no alterations are necessary. Therefore, it is possible to move onto the next steps.
o	Look at which row has the least number of zeros and assign that point in the matrix and cross out the corresponding column. Follow the same process until each job is assigned.

<p align="center">
<img src="https://i.ibb.co/HfPfHxkR/Screenshot-2026-03-10-at-09-06-18.png"/>
<br/>
</p>

This is successfully done here. As seen above, the idea here is that once, for example, Terri has been assigned to wash, that column (job) is now finished. Therefore, the only other possible job for John is paint. This is ideal as the row ‘John’ also has a zero under ‘Paint’.

The following are the job assignments through the Hungarian Method.
•	John to paint
•	Karen to mow
•	Terri to wash
If this occurs, the total cost would be 9 + 10 + 8 = $27.
It is now appropriate to construct a mathematical model around this problem and it is achieved through spreadsheet modelling.

**Mathematical Model**

This problem is a special kind of transportation problem (possibility of transforming the values into a matrix). More specifically, it is a special kind of least-cost problem as it is a minimization objective. Therefore, like project 2, a simple LP model can be generated to find a solution (‘Superprof’,2019).  The solution is found through the following steps.

•	Objective function
With the objective of minimizing total cost, the following is the objective function of the model with the decision variables being the weights of each potential cost to Klyne (Xi).

Minimize C= 15X1 + 9X2 + 10X3 + 10X4 + 15X5 + 12X6 + 9X7 + 10X8 + 8X9

Subject to, constraints on how many jobs each child can do and how many children are allowed to take on each job,

X1 + X2 + X3 = 1
X4 + X5 + X6 = 1
X7 + X8 + X9 =1

X1 + X4 + X7 = 1
X2 + X5 + X8 = 1
X3 + X6 + X9 =1

•	Spreadsheet modelling 
The following result was achieved through this method.

<p align="center">
<img src="https://i.ibb.co/pvMBMyrS/Screenshot-2026-03-10-at-09-06-37.png"/>
<br/>
<img src="https://i.ibb.co/1fV7Mgv4/Screenshot-2026-03-10-at-09-06-50.png"/>
<br/>  
</p>

It is found that the total cost is $27.

Conclusion

Both the Hungarian and the LP model have produced the same result that assigning Karen to mow, John to paint and Terri to wash and minimize the total cost to $27. It can be said the Hungarian is ideal for this kind of assignment problem because it usually finds an optimal solution for simple issues like Klyne’s and is faster than complex LP models (‘Stack Exchange’,2022). However, if a situation was to become larger and have many more constraints, a LP model would be more accurate. Spreadsheet models are also more flexible as it is a program and therefore, it is only necessary to input new values to change the outcome completely. Additionally, it is not too difficult to add and alter constraints or the program (‘Stack Exchange’,2022).
With this information, it is recommended that both approaches should be used they have many differences and therefore complement each other in tackling any assignment problems in the future.
