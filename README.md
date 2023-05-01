Download Link: https://assignmentchef.com/product/solved-cis1300-assignment-1-a-temporal-challenge
<br>
<em>Time, time, time, see what’s become of me While I looked around for my possibilities… </em>A Hazy Shade of Winter (Paul Simon)




<h1>Introduction</h1>




Today is Saturday, September 14, 2019 and the exam for CIS1300 is on December 9, 2019.  How many days do you have before the exam?  Well, you have 86 days!  This count includes today but does not include the day of the exam.  In other words:

<h1>From and including: Saturday, September 14, 2019 To, but not including Monday, December 9, 2019</h1>

Wouldn’t it be nice to be able to ask how many days separated any two days?  Wait no more, you are going to write this wonderfully useful program as your first assignment in CIS1300!




<h1>Functionality</h1>




You will write this program in increasingly more powerful forms.  At each stage you will earn a grade so that it you do all stages you can earn 100% but if you cannot finish the last stage you can earn 80%.




For Stages A to D, both the <strong>start date</strong> and the <strong>end date</strong> are in the <strong>same</strong> year.




<strong>[60%] </strong>Stage A)  ./daysCalculatorA dd1 mm1 yyyy1 dd2 mm2 yyyy2    where dd1 mm1 yyyy1 represents the start date and dd2 mm2 yyyy2 represents the end date.  The program returns the number of days for

From and including: <strong>Start Date</strong>

To, but <strong>not</strong> including <strong>End Date</strong>

The output format is just the number.  For example,

$ ./daysCalculatorA  14 9 2019  9 12 2019

86

$




<strong>[75%]</strong> Stage B)  ./daysCalculatorB dd1 mm1 yyyy1 dd2 mm2 yyyy2 include   where dd1 mm1 yyyy1 represents the start date and dd2 mm2 yyyy2 represents the end date and the string “include” tells the program to return the value for

From and including: <strong>Start Date</strong>

To, and including <strong>End Date</strong>

If include is not on the command line, the program will return the value for

From and including: <strong>Start Date</strong>

To, but <strong>not</strong> including <strong>End Date</strong>




This stage must also test that the start date occurs before the end date.




<strong>[85%]</strong> Stage C)  ./daysCalculatorC dd1-mm1-yyyy1 dd2-mm2-yyyy2 include

where “dd1-mm1-yyyy1” represents the start date as a string and “dd2-mm2-yyyy2” represents the end date as a string and the string “include” tells the program to return the value for

From and including: <strong>Start Date</strong>

To, and including <strong>End Date</strong>

If include is not on the command line, the program will return the value for

From and including: <strong>Start Date</strong>

To, but <strong>not</strong> including <strong>End Date</strong>




<strong>[90%]</strong> Stage D)  ./daysCalculatorD today dd2-mm2-yyyy2 include

<strong>OR</strong>         ./daysCalculatorD dd1-mm1-yyyy1 today include

This is the same as Stage C except that either of the dates can be the string “today”




<strong>[100%]</strong> Stage E)  ./daysCalculatorE dd1-mm1-yyyy1 dd2-mm2-yyyy2 include

This is the same as Stage C but the start date and the end date can be in <strong>different</strong> years.  Remember some of the years can be leap years.




<h1>Information That You Will Need</h1>




How can you calculate the number of days between two days?  Instead of using the date format dd-mm-yyyy, you translate the date into the Day-of-Year.  Day-of-Year is a number for a date that uses the month and the day.  You start by giving January 1 the value 1 and label all other days by adding 1 for each day in order.  In other words, January 1 = 1, January 2 = 2, …, August 1 = 213, …, December 31 = 365.  This is true if the year in question is not a leap year.  If the year was a leap year than in the previous list, August 1 would be 214 and December 31 would be 366.




The following table contains the <strong>Day-of-Year</strong> value for the first day of each month in a <strong>non-leap year</strong>:

<table width="623">

 <tbody>

  <tr>

   <td width="208">Jan: 1</td>

   <td width="208">May: 121</td>

   <td width="208">Sep: 244</td>

  </tr>

  <tr>

   <td width="208">Feb: 32</td>

   <td width="208">Jun: 152</td>

   <td width="208">Oct: 274</td>

  </tr>

  <tr>

   <td width="208">Mar: 60</td>

   <td width="208">Jul: 182</td>

   <td width="208">Nov: 305</td>

  </tr>

  <tr>

   <td width="208">Apr: 91</td>

   <td width="208">Aug: 213</td>

   <td width="208">Dec: 335</td>

  </tr>

 </tbody>

</table>




The following table contains the <strong>Day-of-Year</strong> value for the first day of each month in a <strong>leap year</strong>:

<table width="623">

 <tbody>

  <tr>

   <td width="208">Jan: 1</td>

   <td width="208">May: 122</td>

   <td width="208">Sep: 245</td>

  </tr>

  <tr>

   <td width="208">Feb: 32</td>

   <td width="208">Jun: 153</td>

   <td width="208">Oct: 275</td>

  </tr>

  <tr>

   <td width="208">Mar: 61</td>

   <td width="208">Jul: 183</td>

   <td width="208">Nov: 306</td>

  </tr>

  <tr>

   <td width="208">Apr: 92</td>

   <td width="208">Aug: 214</td>

   <td width="208">Dec: 336</td>

  </tr>

 </tbody>

</table>




On <u>https://nsidc.org/data/tools/doy_calendar.html</u> you will find a nice graphic showing all of the Day-of-Year for each day of the year for non-leap years and leap years.

<h1>Checking Your Work</h1>




To check your work you can use the following Days Calculator: Days Calculator: Days Between Two Dates https://www.timeanddate.com/date/durationresult.html