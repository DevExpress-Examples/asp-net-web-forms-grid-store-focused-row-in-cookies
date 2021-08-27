<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128535912/13.2.6%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E5089)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [Default.aspx](./CS/WebSite/Default.aspx) (VB: [Default.aspx](./VB/WebSite/Default.aspx))
* [Default.aspx.cs](./CS/WebSite/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/WebSite/Default.aspx.vb))
<!-- default file list end -->
# ASPxGridView - How to store a focused row index in cookies
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e5089/)**
<!-- run online end -->


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


