hachi-lab
=========
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace coloringnew
{
    public partial class Form2 : Form
    {
        public Form2()
        {
            InitializeComponent();
        }

        string n;
        Int16 n1;
        Rectangle[] r = new Rectangle[20];
        int i,j;
        double y;
        
        Graphics g;
       // Rectangle r, r1,r2;
        int h1, h2;
        Pen p;
        Random x1 = new Random();
        Graphics gr;
        string text1, text2, text3,text4;
         
        private void button1_Click(object sender, EventArgs e)
        {
           // r.X = x1.Next(10, 500);
            //r.Y = x1.Next(20, 520);
            //r1.X = x1.Next(100, 700);
            //r1.Y = x1.Next(120, 720);

            n = textBox1.Text;
            n1 = Convert.ToInt16(n);
            
            
            g = CreateGraphics();
            p = new Pen(Brushes.DarkBlue);
            h1 = 10;
            for(j=0;j<3;j++)
            {
                h2 = (j * 100);
                r[i] = new Rectangle(h1 , h2, 30, 30);
                g.DrawRectangle(p, r[i]);
            }

            h1=100;
            h2 = 0;
                for(i=3;i<n1;i++)
                {
                    h2= (i * 50);
                  //  h1 = h1 + 100;
             //  h1 = (20*(i+i));
               //h2= (40*(i+i))+5;
               
                //r[i]=new Rectangle();
                r[i] = new Rectangle(h1 , h2, 30, 30);
               // r[i+1] = new Rectangle((i+1) * (4 + 40), (i+2) * (5 + 80), 30, 20);
                g.DrawRectangle(p, r[i]);
               // g.DrawRectangle(p, r[i+1]);
            }
                

            

            //0-1
            if (Convert.ToDouble(tB3.Text) == 1)
            {
                g.DrawRectangle(p, r[0]);
                Point pt1 = new Point(10, 5);
                Point pt2 = new Point(10, 100);
                g.DrawLine(p, pt1, pt2);
                g.DrawRectangle(p, r[1]);
            }


            //0-2
            if (Convert.ToDouble(tB4.Text) == 1)
            {
                g.DrawRectangle(p, r[0]);
                Point pt3 = new Point(10, 15);
                Point pt4 = new Point(15, 210);
                g.DrawLine(p, pt3, pt4);
                g.DrawRectangle(p, r[2]);
            }

            //1-2
            if (Convert.ToDouble(tB6.Text) == 1)
            {
                g.DrawRectangle(p, r[1]);
                Point pt5 = new Point(11, 100);
                Point pt6 = new Point(10, 200);
                g.DrawLine(p, pt5, pt6);
                g.DrawRectangle(p, r[2]);
            }

            //1-3
            if (Convert.ToDouble(tB7.Text) == 1)
            {
                g.DrawRectangle(p, r[1]);
                Point pt7 = new Point(12, 110);
                Point pt8 = new Point(100, 150);
                g.DrawLine(p, pt7, pt8);
                g.DrawRectangle(p, r[3]);
            }


            //0-3
            if (Convert.ToDouble(tB5.Text) == 1)
            {
                g.DrawRectangle(p, r[0]);
                Point pt9 = new Point(10, 15);
                Point pt10 = new Point(105, 150);
                g.DrawLine(p, pt9, pt10);
                g.DrawRectangle(p, r[3]);
            }
            //0-4
            if (Convert.ToDouble(tB10.Text) == 1)
            {
                g.DrawRectangle(p, r[0]);
                Point pt9 = new Point(10, 14);
                Point pt10 = new Point(110, 200);
                g.DrawLine(p, pt9, pt10);
                g.DrawRectangle(p, r[3]);
            }

            //2-3
            if (Convert.ToDouble(tB8.Text) == 1)
            {
                g.DrawRectangle(p, r[2]);
                Point pt11 = new Point(12, 200);
                Point pt12 = new Point(105, 150);
                g.DrawLine(p, pt11, pt12);
                g.DrawRectangle(p, r[3]);
            }

            //1-4
            if (Convert.ToDouble(tB12.Text) == 1)
            {
                g.DrawRectangle(p, r[1]);
                Point pt13 = new Point(15, 115);
                Point pt14 = new Point(115, 205);
                g.DrawLine(p, pt13, pt14);
                g.DrawRectangle(p, r[4]);
            }

            //2-4
            if (Convert.ToDouble(tB14.Text) == 1)
            {
                g.DrawRectangle(p, r[2]);
                Point pt15 = new Point(12, 205);
                Point pt16 = new Point(115, 205);
                g.DrawLine(p, pt15, pt16);
                g.DrawRectangle(p, r[4]);
            }

            //3-4
            if (Convert.ToDouble(tB16.Text) == 1)
            {
                g.DrawRectangle(p, r[3]);
                Point pt17 = new Point(105, 150);
                Point pt18 = new Point(115, 200);
                g.DrawLine(p, pt17, pt18);
                g.DrawRectangle(p, r[4]);
            }

            

            
            
                text1 = "green";
                using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                {
                    // RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                    g.DrawString(text1, font1, Brushes.Green, r[0]);
                    g.DrawRectangle(Pens.Black, Rectangle.Round(r[0]));
                }


                if (text1 == "green" && n1>=2)
                {
                    text2 = "red";
                    using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                    {
                        //  RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                        g.DrawString(text2, font1, Brushes.Red, r[1]);
                        g.DrawRectangle(Pens.Black, Rectangle.Round(r[1]));
                    }
                    
                }


                

                    if (text1 == "green" && text2 == "red" && n1>=3)
                    {
                        text3 = "blue";
                        using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                        {
                            //  RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                            g.DrawString(text3, font1, Brushes.Blue, r[2]);
                            g.DrawRectangle(Pens.Black, Rectangle.Round(r[2]));
                        }
                    }
               


            //for 4 nodes
                if (n1 >= 4)
                {


                    if ((Convert.ToDouble(tB7.Text) ==1 && Convert.ToDouble(tB8.Text) == 1) && (Convert.ToDouble(tB5.Text) ==0))
                    {
                        text3 = "green";
                        using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                        {
                            //  RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                            g.DrawString(text3, font1, Brushes.Green, r[3]);
                            g.DrawRectangle(Pens.Black, Rectangle.Round(r[3]));
                        }
                    }

                    if ((Convert.ToDouble(tB7.Text) == 1 && Convert.ToDouble(tB8.Text) == 1 && Convert.ToDouble(tB5.Text) == 1))
                    {
                        text3 = "gray";
                        
                        using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                        {
                            //  RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                            g.DrawString(text3, font1, Brushes.Gray, r[3]);
                            g.DrawRectangle(Pens.Black, Rectangle.Round(r[3]));
                        }
                    }

                    if (Convert.ToDouble(tB7.Text) ==1 && (Convert.ToDouble(tB5.Text) ==0 && Convert.ToDouble(tB8.Text) == 0))
                    {
                        text3 = "green";
                        using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                        {
                            //  RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                            g.DrawString(text3, font1, Brushes.Green, r[3]);
                            g.DrawRectangle(Pens.Black, Rectangle.Round(r[3]));
                        }
                    }

                    if (Convert.ToDouble(tB7.Text) ==1 && Convert.ToDouble(tB5.Text) ==1 && (Convert.ToDouble(tB8.Text) ==0))
                    {
                        text3 = "blue";
                        using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                        {
                            //  RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                            g.DrawString(text3, font1, Brushes.Blue, r[3]);
                            g.DrawRectangle(Pens.Black, Rectangle.Round(r[3]));
                        }
                    }
                }

            
                if (n1 == 5)
                {
                    
                    
                    
                    if ( ( Convert.ToDouble(tB14.Text) == 1 &&  Convert.ToDouble(tB16.Text) == 1 &&  (Convert.ToDouble(tB10.Text) == 0) && (Convert.ToDouble(tB12.Text) == 0))|| (Convert.ToDouble(tB14.Text) == 1 && (Convert.ToDouble(tB16.Text) == 0)&& (Convert.ToDouble(tB10.Text) == 0) && (Convert.ToDouble(tB12.Text) == 0)) || (Convert.ToDouble(tB14.Text) == 1  && Convert.ToDouble(tB16.Text) == 1  && (Convert.ToDouble(tB10.Text) == 0) && (Convert.ToDouble(tB12.Text) == 0)))
                    {
                        text3 = "red";
                        using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                        {
                            //  RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                            g.DrawString(text3, font1, Brushes.Red, r[4]);
                            g.DrawRectangle(Pens.Black, Rectangle.Round(r[4]));
                        }
                    }

                    if (( Convert.ToDouble(tB12.Text) == 1 && Convert.ToDouble(tB16.Text) == 0 && (Convert.ToDouble(tB10.Text) == 0) && (Convert.ToDouble(tB14.Text) == 0) ) || ( Convert.ToDouble(tB14.Text) == 1  && Convert.ToDouble(tB16.Text) == 0  && (Convert.ToDouble(tB10.Text) == 0) && (Convert.ToDouble(tB12.Text) == 0) ) || ( Convert.ToDouble(tB14.Text) == 1  && Convert.ToDouble(tB16.Text) == 0  && (Convert.ToDouble(tB10.Text) == 0) && (Convert.ToDouble(tB12.Text) == 1)))
                    {
                        text3 = "green";
                        using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                        {
                            //  RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                            g.DrawString(text3, font1, Brushes.Green, r[4]);
                            g.DrawRectangle(Pens.Black, Rectangle.Round(r[4]));
                        }
                    }

                    if (( Convert.ToDouble(tB14.Text) == 1 && Convert.ToDouble(tB16.Text) == 1  && (Convert.ToDouble(tB10.Text) == 0) && (Convert.ToDouble(tB12.Text) == 0)))
                    {
                        text3 = "red";
                        using (Font font1 = new Font("Arial", 12, FontStyle.Bold, GraphicsUnit.Point))
                        {
                            //  RectangleF rectF1 = new RectangleF(60, 70, 100, 122);
                            g.DrawString(text3, font1, Brushes.Red, r[4]);
                            g.DrawRectangle(Pens.Black, Rectangle.Round(r[4]));
                        }
                    }
                    
                }
            
        
        }

        private void textBox3_TextChanged(object sender, EventArgs e)
        {
            
        }

        private void button2_Click(object sender, EventArgs e)
        {
         
        }

        private void Form2_Load(object sender, EventArgs e)
        {

        }

        private void textBox2_TextChanged(object sender, EventArgs e)
        {

        }
    }
}
