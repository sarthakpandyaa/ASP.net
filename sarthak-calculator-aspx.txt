<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="calculator form.aspx.cs" Inherits="_1_7291_nitin_calculator.calculator_form" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    <style type="text/css">
        .auto-style1 {
            width: 100%;
            height: 227px;
        }
        .auto-style2 {
            height: 23px;
        }
        .auto-style3 {
            height: 21px;
        }
    </style>
</head>
<body>
    <form id="form1" runat="server" align="center">
        <asp:Label ID="Label5" runat="server" Text="calculator form"></asp:Label>
        <div>
        </div>
        <table class="auto-style1">
            <tr>
                <td align="right">
                    <asp:Label ID="Label1" runat="server" Text="enter first number"></asp:Label>
                </td>
                <td align="left">
                    <asp:TextBox ID="TextBox1" runat="server"></asp:TextBox>
                </td>
            </tr>
            <tr align="right">
                <td class="auto-style2">
                    <asp:Label ID="Label2" runat="server" Text="enter second number"></asp:Label>
                </td>
                <td class="auto-style2" align="left">
                    <asp:TextBox ID="TextBox2" runat="server"></asp:TextBox>
                </td>
            </tr>
            <tr>
                <td class="auto-style3" align="right">
                    <asp:Button ID="Button1" runat="server" Text="ADD" />
                </td>
                <td class="auto-style3" align="left">
                    <asp:Button ID="Button2" runat="server" Text="SUBTRACT" />
                </td>
            </tr>
            <tr align="right">
                <td class="auto-style3">
                    <asp:Button ID="Button4" runat="server" Text="MUL" />
                </td>
                <td class="auto-style3" align="left">
                    <asp:Button ID="Button3" runat="server" style="margin-bottom: 0px" Text="DIV" />
                </td>
            </tr>
            <tr>
                <td class="auto-style3">
                    <asp:Button ID="Button5" runat="server" Text="Button" />
                </td>
                <td class="auto-style3">&nbsp;</td>
            </tr>
        </table>
    </form>
</body>
</html>
