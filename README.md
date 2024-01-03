# AP_1402_2_13
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace AP_1402_2_11.CS
{
    internal class Program
    {
        static void Main(string[] args)
        {
            //برنامه ای بنویسید که 3 عدد را خوانده و عدد اول و دوم را که مجموع ارقام آن برابر اعداد سوم است را نمایش دهد
              int sum(int num)
            {
                int sum=0;
                while(num>0)
                {
                    sum += num % 10;
                    num /= 10;
                }
                return sum;
            }
            void main()
            {
               
                Console.WriteLine("please enter 3 number:");
                 int num1= Convert.ToInt32(Console.ReadLine());
                 int num2 = Convert.ToInt32(Console.ReadLine());
                int targetSum = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Number with sum of digits" + targetSum + " " + num1 + " " + num2 + " ");
                for(int i=num1;i<=num2;i++)
                {
                    if(sum(i)==targetSum)
                    {
                        Console.WriteLine(i + " ");
                    }
                }
                Console.WriteLine();
            }
        }
    }
}
