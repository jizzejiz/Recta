using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Unittest
{
    
            public class Rectangle
            {
                private int length;
                private int width;




                public Rectangle()
                {

                    length = 1;
                    width = 1;

                }

                public Rectangle(int length, int width)
                {
                    this.length = length;
                    this.width = width;

                }

                public int Getlength()
                {
                    return length;
                }

                public int Setlength(int length)
                {
                    this.length = length;
                    return this.length;

                }

                public int Getwidth()
                {
                    return width;
                }

                public int Setwidth(int width)
                {
                    this.width = width;
                    return this.width;
                }

                public int GetPerimeter()
                {
                    return (width * 2) + (length * 2);

                }

                public int GetArea()
                {
                    return length * width;
                }
        }
    }




