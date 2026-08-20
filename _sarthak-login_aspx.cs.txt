using System;
using System.Configuration;
using System.Data.SqlClient;

namespace login_form
{
    public partial class login_form : System.Web.UI.Page
    {
        protected void Page_Load(object sender, EventArgs e)
        {
        }

        protected void submit_Click(object sender, EventArgs e)
        {
            string username = user.Text.Trim();
            string password = pass.Text.Trim();

            if (username == "" || password == "")
            {
                Response.Write("<script>alert('Please enter username and password');</script>");
                return;
            }

            string conString = ConfigurationManager
                .ConnectionStrings["LoginDB"]
                .ConnectionString;

            using (SqlConnection con = new SqlConnection(conString))
            {
                string query = @"Data Source=(LocalDB)\MSSQLLocalDB;AttachDbFilename=C:\TEST\login_form\login_form\App_Data\login_form.mdf;Integrated Security=True";

                using (SqlCommand cmd = new SqlCommand(query, con))
                {
                    cmd.Parameters.AddWithValue("@Username", username);
                    cmd.Parameters.AddWithValue("@Password", password);

                    con.Open();

                    SqlDataReader reader = cmd.ExecuteReader();

                    if (reader.Read())
                    {
                        Session["UserId"] = reader["UserId"].ToString();
                        Session["Username"] = reader["Username"].ToString();
                        string role = reader["Role"].ToString();

                        if (role == "Admin")
                        {
                            Response.Redirect("AdminDashboard.aspx");
                        }
                        else if (role == "User")
                        {
                            Response.Redirect("UserDashboard.aspx");
                        }
                        else
                        {
                            Response.Write("<script>alert('Invalid user role');</script>");
                        }
                    }
                    else
                    {
                        Response.Write("<script>alert('Invalid username or password');</script>");
                    }

                    con.Close();
                }
            }
        }

        protected void clear_Click(object sender, EventArgs e)
        {
            user.Text = "";
            pass.Text = "";
        }
    }
}