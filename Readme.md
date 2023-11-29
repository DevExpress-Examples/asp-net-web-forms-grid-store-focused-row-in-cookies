<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128535912/13.2.6%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E5089)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->

# Grid View for ASP.NET Web Forms - How to store a focused row index in cookies
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e5089/)**
<!-- run online end -->


[ASPxGridView](https://docs.devexpress.com/AspNet/DevExpress.Web.ASPxGridView) does not save a focused row in cookies. This example demonstrates how to save and restore a focused row index to cookies.

```js
function OnFocusedRowChanged(s, e) {
	ASPxClientUtils.SetCookie(s.name + '_focudedIndex', s.GetFocusedRowIndex());
}
function OnInit(s, e) {
	if (ASPxClientUtils.GetCookie(s.name + '_focudedIndex') != null)
		s.SetFocusedRowIndex(ASPxClientUtils.GetCookie(s.name + '_focudedIndex'));
}
```

## Files to Review

* [Default.aspx](./CS/WebSite/Default.aspx) (VB: [Default.aspx](./VB/WebSite/Default.aspx))
* [Default.aspx.cs](./CS/WebSite/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/WebSite/Default.aspx.vb))
