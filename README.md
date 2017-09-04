# Catch-the-Thief
Just another repository
using System;

namespace _6.Catch_the_Thief
{
    class Program
    {
        static void Main(string[] args)
        {
            string numeralType = Console.ReadLine();
            int n = int.Parse(Console.ReadLine());
            long thiefIds = long.MinValue;

            for (int i = 0; i < n; i++)
            {
                long id = long.Parse(Console.ReadLine());

                if (numeralType == "sbyte")
                {
                    if (id > thiefIds && id <= sbyte.MaxValue)
                    {
                        thiefIds = id;
                    }
                }
                else if (numeralType == "int")
                {
                    if (id > thiefIds && id <= int.MaxValue)
                    {
                        thiefIds = id;
                    }
                }
                else if (numeralType == "long")
                {
                    if (id > thiefIds && id <= long.MaxValue)
                    {
                        thiefIds = id;
                    }
                }
            }

            Console.WriteLine(thiefIds);
        }
    }
}
