<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="login form.aspx.cs" Inherits="login_form.login_form" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    <style type="text/css">
        .auto-style1 {
            width: 100%;
        }
        .auto-style2 {
            height: 23px;
        }
    </style>
</head>
<body>
    <form id="form1" runat="server">
        <div align="center">
            <asp:Label ID="Label1" runat="server" Text="LOGIN FORM"></asp:Label>
        </div>
        <table class="auto-style1">
            <tr align="right">
                <td class="auto-style2">
                    <asp:Label ID="Label2" runat="server" Text="Username"></asp:Label>
                </td>
                <td class="auto-style2" align="left">
                    <asp:TextBox ID="user" runat="server"></asp:TextBox>
                </td>
            </tr>
            <tr>
                <td align="right">
                    <asp:Label ID="Label3" runat="server" Text="Password"></asp:Label>
                </td>
                <td>
                    <asp:TextBox ID="pass" runat="server"></asp:TextBox>
                </td>
            </tr>
            <tr>
                <td align="right">
                    <asp:Button ID="submit" runat="server" Text="Submit" />
                </td>
                <td>
                    <asp:Button ID="clear" runat="server" Text="Clear" />
                </td>
            </tr>
        </table>
    </form>
</body>
</html>
