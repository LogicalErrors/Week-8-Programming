# Week-8-Programming
Week 8 Programming Code


using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Module8ProjectOfArrays
{
    public partial class frmSunArray : Form
    {
        

        public frmSunArray()
        {
            InitializeComponent();
        }

        private void btnExit_Click(object sender, EventArgs e)
        {
            this.Close();
        }

        private void btnRestArray_Click(object sender, EventArgs e)
        {
            {
                Array.Clear(numbers, 0, numbers.Length);
            }
        }

        private void txtBox1_TextChanged(object sender, EventArgs e)
        {

        }
        int[] numbers = new int[17];
        int i = 0;
        private void btnAdd_Click(object sender, EventArgs e)
        {
            int[] numbers = new int[17];
            int i = 0;
            {

                if (i < 17)
                {
                    if (int.Parse(textBox1.Text) >= 1125)
                    {
                        label3.Text = "Number entered is out of range";
                    }
                    else if (int.Parse(textBox1.Text) <= -1125)
                    {
                        label3.Text = "Number entered is too small";
                    }
                    else
                    {
                        numbers[i] = int.Parse(textBox1.Text);
                        i++;
                    }
                }
                else
                {
                    label3.Text = "Array is full, clear array";
                }
                textBox1.Text = "";
            }
        }

        private void btnShowStatistics_Click(object sender, EventArgs e)
        {
            {
                label1.Text = string.Join(",", numbers);
            }
        }

        private void lblArrayDisplay_Click(object sender, EventArgs e)
        {

        }

        private void lblStatsBox_Click(object sender, EventArgs e)
        {

        }
    }
}
