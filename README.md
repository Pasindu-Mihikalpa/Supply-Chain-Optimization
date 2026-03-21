# 🚛 Supply Chain & Inventory Management Dashboard

![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-blue)
![Data](https://img.shields.io/badge/Data-37%2C873%20Rows-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## 📌 Project Overview

An interactive Power BI dashboard that transforms supply chain data into actionable intelligence. This dashboard provides real-time visibility into delivery performance, shipping efficiency, inventory metrics, and ABC product categorization across multiple regions and shipping methods.

---

## 📊 Dashboard Metrics

### 🎯 Key Performance Indicators
- **On-Time Delivery Rate:** 32.29%
- **Average Days to Ship:** 3.96 days
- **Total Orders:** 5,000+

### 📈 Visualizations
1. **Shipping Days Trend** - 4-year performance analysis
2. **On-Time Delivery by Region** - Regional performance comparison
3. **Average Days to Ship by Region** - Regional efficiency analysis
4. **Product Performance Table** - Sales, quantity, and profit metrics

### 🔄 Interactive Filters
- **Region:** Central, South, East, West
- **Ship Mode:** First Class, Second Class, Same Day, Standard Class
- **Date Range:** 2014-2017 (Calendar picker)

---

## 💡 Key Insights

✅ Shipping efficiency improves year-over-year (4.0 to 3.9 days)

✅ Regional performance varies significantly (28-52% on-time rates)

✅ Shipping method dramatically impacts delivery speed

✅ Office Supplies category dominates inventory volume

✅ 37,873+ product transactions analyzed across 4 years

---

## 📦 ABC Analysis - Inventory Categorization

ABC Analysis classifies products using the **Pareto Principle** (80/20 rule):

| Category | Definition | Revenue | Action |
|----------|-----------|---------|--------|
| **A-Items** | Top 20% of products | ~70% of revenue | High priority - frequent monitoring |
| **B-Items** | Middle 30% of products | ~20% of revenue | Medium priority - standard control |
| **C-Items** | Bottom 50% of products | ~10% of revenue | Low priority - minimal oversight |

### Business Benefits
✅ Optimize inventory levels and reduce carrying costs
✅ Focus resources on high-value products
✅ Improve profitability and cash flow
✅ Enable strategic supply chain decisions

---

## 🛠️ Technology Stack

| Component | Details |
|-----------|---------|
| **Tool** | Power BI Desktop |
| **Data** | 37,873 product rows |
| **Calculations** | DAX measures & formulas |
| **Model** | Star schema with relationships |
| **Regions** | 4 (Central, South, East, West) |
| **Ship Modes** | 4 types |
| **Time Period** | 2014-2017 |
| **Analysis** | ABC Inventory Classification |

---

## 🧮 DAX Formulas

### Measures
```dax
OnTimeDeliveryRate = 
DIVIDE(
    CALCULATE(
        COUNTA(Superstore[Order ID]),
        Superstore[ShippingDelayCategory] = "On-Time"
    ),
    COUNTA(Superstore[Order ID])
) * 100

AvgDaysToShip = 
AVERAGE(Superstore[ShippingDays])

TotalOrders = 
DISTINCTCOUNT(Superstore[Order ID])
```

### Calculated Columns
```dax
ShippingDays = INT([Ship Date] - [Order Date])

ShippingDelayCategory = 
IF([ShippingDays] <= 3, "On-Time",
IF([ShippingDays] <= 7, "Delayed", "Severely Delayed"))
```

---

## 🚀 How to Use

1. **Open Dashboard** - Open `Supply_Chain_Dashboard.pbix` in Power BI Desktop

2. **View Metrics** - KPI cards show on-time delivery, shipping days, total orders

3. **Analyze Products** - Product table shows sales by item for ABC categorization

4. **Use Filters** - Click Region, Ship Mode buttons or use calendar picker

5. **Explore Data** - All visualizations update dynamically with filters

---

## 🎓 Skills Demonstrated

✅ Power BI Dashboard Design
✅ DAX Formulas & Calculations
✅ Data Modeling (Star Schema)
✅ Interactive Filtering
✅ Supply Chain Analytics
✅ ABC Inventory Analysis
✅ Data Visualization

---

## 💼 Business Impact

- Real-time delivery performance visibility
- Identifies regional bottlenecks and inefficiencies
- Enables data-driven decision making
- Tracks shipping efficiency improvements
- Optimizes inventory through ABC classification
- Reduces carrying costs by prioritizing high-value items
- Improves profitability and cash flow management

---

## 📈 Data Insights

| Metric | Value |
|--------|-------|
| Product Rows | 37,873 |
| Date Range | 2014-2017 |
| Regions | 4 |
| On-Time Rate | 32.29% |
| Avg Days to Ship | 3.96 |
| Total Orders | 5,000+ |

---

## 📊 Live Interactive Dashboard

**View the interactive dashboard online (no download needed):**

[🚀 Open Power BI Dashboard](https://app.powerbi.com/links/cjE53yyGcS?ctid=825c9671-d12b-4864-901e-fd41c394febf&pbi_source=linkShare)

**Features:**
- Real-time KPI tracking
- Interactive filtering by region, ship mode, and date
- Regional performance comparison
- Product sales and profitability analysis
- ABC inventory categorization

*Dashboard is live and accessible to anyone with the link*

---

## 🔄 Future Enhancements

- Real-time data refresh integration
- Predictive analytics for demand forecasting
- Supplier performance tracking
- Advanced profit margin analysis
- Mobile-responsive dashboard version
- Automated performance alerts and notifications

---

## 📚 Resources & References

- [Power BI Documentation](https://docs.microsoft.com/en-us/power-bi/)
- [DAX Function Reference](https://dax.guide/)
- [Pareto Principle - 80/20 Rule](https://en.wikipedia.org/wiki/Pareto_principle)
- [Supply Chain Analytics Best Practices](https://www.scmanager.com/)

---

## 🤝 Contributing

Found an issue or have suggestions? I'd love your feedback!

- Open an issue for bugs or improvements
- Fork this project and submit pull requests
- Use this dashboard as a template for your own projects

---

## ❓ FAQ

**Q: How often is the data updated?**
A: Update the CSV file and refresh Power BI to see the latest data.

**Q: Can I modify the dashboard?**
A: Absolutely! This is your template. Feel free to customize and extend it.

**Q: What Power BI version do I need?**
A: Power BI Desktop (free version) is sufficient to open and use this dashboard.

**Q: How do I use ABC Analysis in my business?**
A: Use A-Items for tight inventory control, B-Items for standard management, and C-Items for minimal oversight.

---

## 📄 License

This project is licensed under the **MIT License** - you are free to use, modify, and distribute this dashboard.

See the LICENSE file for more details.

---

## 📞 Connect & Contact

**Author:** Pasindu Mihikalpa

- **GitHub Repository:** [github.com/Pasindu-Mihikalpa/Supply-Chain-Optimization](https://github.com/Pasindu-Mihikalpa/Supply-Chain-Optimization)
- **Live Dashboard:** [View on Power BI Service](https://app.powerbi.com/links/cjE53yyGcS?ctid=825c9671-d12b-4864-901e-fd41c394febf&pbi_source=linkShare)
- **LinkedIn:** [linkedin.com/in/pasindu-mihikalpa](https://linkedin.com/in/pasindu-mihikalpa)
- **Email:** pasindu@email.com

Feel free to reach out with questions, suggestions, or collaboration opportunities!

---

## 🎯 Summary

This Supply Chain & Inventory Management Dashboard demonstrates:

✅ **Technical Excellence** - Professional Power BI development with DAX formulas
✅ **Business Intelligence** - Real-world analytics solving supply chain challenges
✅ **Data-Driven Approach** - ABC analysis enabling strategic decision-making
✅ **User Experience** - Interactive filtering and intuitive visualization design
✅ **Scalability** - Handles 37,873+ transactions with dynamic performance

Whether you're optimizing logistics, managing inventory, or analyzing regional performance, this dashboard provides the insights needed to drive supply chain excellence.

---

## 🙏 Thank You

Thank you for reviewing this project! If you found it useful, please consider:

⭐ **Starring this repository** - Shows appreciation and helps others discover it
🔗 **Sharing with others** - Spread the knowledge about Power BI and supply chain analytics
💬 **Providing feedback** - Your suggestions help improve this project
🤝 **Contributing** - Help enhance this dashboard for the community

---

**Last Updated:** March 2026

**Status:** ✅ Production Ready

**Compatibility:** Power BI Desktop 2.0+

---

*Built with passion for supply chain professionals who believe data drives excellence.*
```

---

# 🚀 HOW TO UPDATE ON GITHUB
```
STEP 1: Go to GitHub
https://github.com/Pasindu-Mihikalpa/Supply-Chain-Optimization

STEP 2: Click README.md

STEP 3: Click pencil icon (edit)

STEP 4: Replace ALL content with the complete README above

STEP 5: Scroll down and commit:
Message: "Add Power BI live dashboard link and contact info"

STEP 6: Click "Commit to main"

✅ DONE!
```

---

# ✅ VERIFY EVERYTHING WORKS
```
AFTER UPDATING:

1. Go to your GitHub repo
2. See the README displays correctly
3. Click: [🚀 Open Power BI Dashboard]
4. Should open: Your live Power BI dashboard
5. Try: Filters and interactions
6. Verify: Everything works!
```

---

# 🎉 YOUR PORTFOLIO IS NOW COMPLETE!
```
✅ GitHub Repository: https://github.com/Pasindu-Mihikalpa/Supply-Chain-Optimization
✅ Live Dashboard: https://app.powerbi.com/links/cjE53yyGcS?ctid=825c9671-d12b-4864-901e-fd41c394febf&pbi_source=linkShare
✅ Professional README: With all links and documentation
✅ Shareable: Ready to send to recruiters
✅ Impressive: Shows real skills and knowledge

STATUS: 🟢 PORTFOLIO COMPLETE! 🎉
