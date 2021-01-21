
# One-and-Two-Sample-T-Test-using-SAS

/*One sample t-test*/

ods graphics;



proc ttest data=STAT1.ameshousing3

plots(shownull)= interval

H0=135000;

var SalePrice;

title "One Sample t-test whether mean SalePrice=$135,000";

run;



title;



/*Two sample t-test*/

ods graphics;



proc ttest data=stat1.ameshousing3 plots (shownull)=interval;

class Masonry_Veneer;

var SalePrice;

format Masonry_Veneer $NoYes.;

title "Two sample t-test Comparing Masonry Veener, No vs. Yes";

run;



title;





