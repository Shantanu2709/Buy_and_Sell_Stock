# Buy_and_Sell_Stock
Buy_and_Sell_Stock for linear time Complexity...
// Here we are going to find the max profit...
//Java Code
public static int Buy_and_Sell_Stock(int [] prices)
{
int n=prices.length;
int buyPrice = Integer.MAX_VALUE;
int MaxProfit =0;
for(int i=0; i<n; i++)
{
//Case 1
  if(buyPrice<prices[i])
 {
int profit = prices[i]-buyPrice;
MaxProfit=Math.max(profit,MaxProfit);
 }
 //Case 2
  if(buyPrice>prices[i])
 {
buyPrice=prices[i];
 }
}
return MaxProfit;
}
