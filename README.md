```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace StructuresC_
{
    internal class Program
    {
       struct Town
        {
           public string TownName;
            public int Population;
            public double Area;
            public string County;

            public Town(string tName,int tPop,double tArea, string tCounty)
            {
                TownName = tName;
                Population = tPop;
                Area = tArea;
                County = tCounty;
            }

        }

        static void Main(string[] args)
        {
            Town t;
            t.TownName = "Hekcmondwike";
            t.Population = 12345;
            t.Area = 6520.5;
            t.County = "West Yorkshire";
            Console.WriteLine(t.TownName);
            Console.WriteLine($"Town {t.TownName} has a population of  {t.Population} and an area of {t.Area}");

            Town Othertown = new Town("Batley",123,63.1,"West Yorkshire");
            Console.WriteLine($"Town {Othertown.TownName} has a population of  {Othertown.Population} and an area of {Othertown.Area}");

            Town[] towns = new Town[6];
            towns[0] = Othertown;
            towns[1] = new Town("Leeds", 111, 12.3, "West Yorkshire");
            towns[2].TownName = "London";
            towns[2].Population = 1;
            towns[2].Area = 1.1;
            towns[2].County = "South";

            Town[] myTowns = new Town[6];
            for (int i = 0; i < 6; i++)
            {
                Console.WriteLine("Town" + i.ToString());
                Console.Write("Enter town name: ");
                myTowns[i].TownName = Console.ReadLine();
                Console.Write("Enter population: ");
                myTowns[i].Population =Convert.ToInt32(Console.ReadLine());
                Console.Write("Enter area: ");
                myTowns[i].Area = Convert.ToDouble(Console.ReadLine());
                Console.Write("Enter county: ");
                myTowns[i].County = Console.ReadLine();
            }
            Town[] myTowns2 = new Town[6];
            string tName, County;
            int pop;
            double area;

            for (int i = 0; i < 6; i++)
            {
                Console.WriteLine("Town" + i.ToString());
                Console.Write("Enter town name: ");
               tName = Console.ReadLine();
                Console.Write("Enter population: ");
                pop = Convert.ToInt32(Console.ReadLine());
                Console.Write("Enter area: ");
                area = Convert.ToDouble(Console.ReadLine());
                Console.Write("Enter county: ");
                County = Console.ReadLine();
                myTowns2[i] = new Town(tName, pop, area, County);
            }


        }
    }
}
```
