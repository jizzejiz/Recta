using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Unittest;
using NUnit.Framework;


namespace RecTest
{
    class testclass
    {
        [Test]

        public void GetLength_input4_expectedLengthEquals4()

        {
            //Arrange
            int l = 4;
            int w = 4;
            Rectangle testRectangle = new Rectangle(l, w);

            //Act

            int length = testRectangle.Getlength();

            //Assert
            Assert.AreEqual(l, length);



        }
        [Test]

        public void GetWidth_input5_expectedWidthEquals5()

        {
            //Arrange
            int l = 3;
            int w = 5;
            Rectangle testRectangle = new Rectangle(l, w);

            //Act

            int width = testRectangle.Getwidth();

            //Assert
            Assert.AreEqual(w, width);


        }
        [Test]

        public void SetWidth_input8_expectedWidthEquals8()

        {
            //Arrange
            int l = 3;
            int w = 8;
            Rectangle testRectangle = new Rectangle(l, w);

            //Act

            int width = testRectangle.Setwidth(w);

            //Assert
            Assert.AreEqual(w, width);


        }

        [Test]

        public void SetLength_input6_expectedLengthEquals6()

        {
            //Arrange
            int l = 6;
            int w = 5;
            Rectangle testRectangle = new Rectangle(l, w);

            //Act

            int width = testRectangle.Setlength(w);

            //Assert
            Assert.AreEqual(w, width);


        }

        [Test]

        public void GetPerimeter_inputlength2_inputwidth_7expectedPerimeterEquals18()

        {
            //Arrange
            int l = 2;
            int w = 7;

            Rectangle testRectangle = new Rectangle(l, w);
            int expectedresult = 2 * (l + w);

            //Act

            int Perimeter = testRectangle.GetPerimeter();

            //Assert
            Assert.AreEqual(expectedresult, Perimeter);

        }
        [Test]

        public void GetArea_inputlength11_inputwidth_12expectedAreaEquals132()

        {
            //Arrange
            int l = 11;
            int w = 12;

            Rectangle testRectangle = new Rectangle(l, w);
            int expectedresult = l * w;

            //Act

            int Area = testRectangle.GetArea();

            //Assert
            Assert.AreEqual(expectedresult, Area);



        }
        }
    }
