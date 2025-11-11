---
title: Final Lecture Notes
summary: "Final lecture code snippets covering event handling, calculations, and Windows Forms button click events"
---

```cs
private void btnCalc_click (object sender, Eventargs e) {
	double GrossSalary = double.Parse (textGrossSalary.Text);
	double GrossSalary = double.Parse (TaxPrecent.Text);

	double TaxAccount = GrossSalary * TaxPrecent;
	double NetSalary = GrossSalary - TaxAmount;
}
```
