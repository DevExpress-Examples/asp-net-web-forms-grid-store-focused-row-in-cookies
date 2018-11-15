<!-- default file list -->
*Files to look at*:

* [Default.aspx](./CS/WebSite/Default.aspx) (VB: [Default.aspx](./VB/WebSite/Default.aspx))
* [Default.aspx.cs](./CS/WebSite/Default.aspx.cs) (VB: [Default.aspx](./VB/WebSite/Default.aspx))
<!-- default file list end -->
# ASPxGridView - How to store a focused row index in cookies


<p>ASPxGridView does not save a focused row in cookies. However, you can add this capability by saving and restoring a focused row index to cookies manually:</p><br />


```js
function OnFocusedRowChanged(s, e) {
	ASPxClientUtils.SetCookie(s.name + '_focudedIndex', s.GetFocusedRowIndex());
}
function OnInit(s, e) {
	if (ASPxClientUtils.GetCookie(s.name + '_focudedIndex') != null)
		s.SetFocusedRowIndex(ASPxClientUtils.GetCookie(s.name + '_focudedIndex'));
}

```

<p><strong>See Also:</strong><br />
<a href="https://www.devexpress.com/Support/Center/p/E5090">ASPxGridView - How to store a focused row index in cookies when ProcessFocusedRowChangedOnServer="true"</a></p>

<br/>


