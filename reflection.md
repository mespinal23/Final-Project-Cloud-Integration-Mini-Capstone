# Reflection

##  <ins>Areas of Confidence</ins>

The part of this project I felt most confident about was defining the problem and explaining why it matters in a real clinical setting. Chemotherapy scheduling and chair utilization are challenges I see regularly, so turning those day-to-day issues into a use case felt very natural. The problem is not hypothetical for me; it directly affects patients, schedulers, and nursing staff. Because of that, it was easy to identify realistic data sources such as nurse staffing levels, scheduled chair time, and actual infusion duration, and to clearly explain how inaccuracies in these areas contribute to last-minute scheduling, unused capacity, and added stress for both staff and patients.

I was also comfortable mapping out the overall data flow and selecting cloud services that fit the needs of this problem. Thinking through how data would move from intake to storage, processing, and analysis felt intuitive, especially since we covered similar patterns throughout the course. Using serverless compute, cloud storage, and a managed database made sense not only from a technical standpoint but also from an operational and cost perspective. These choices reflect how healthcare organizations often approach cloud solutions: focusing on scalability, reliability, and minimizing overhead. Overall, this part of the project allowed me to connect course concepts directly to a real-world healthcare workflow that I already understand well.

## <ins>Areas of Uncertainty</ins>

The area I felt least confident about was how this design would perform at scale in a real clinical environment. While the architecture works well for batch uploads and summary reporting, a production system would need to handle real‑time updates, higher data volumes, and more complex scheduling rules. Those considerations are beyond the scope of this assignment, but they would be important in a real deployment.

I was also less certain about how advanced the analytics should be. For this project, I intentionally kept the analysis simple and focused on descriptive metrics rather than predictive modeling, but a real-world solution would likely require more sophisticated methods.

## <ins>Alternative Architecture Considered</ins>

I considered using a traditional virtual machine to host the application and processing logic. However, I ultimately chose a serverless approach because it reduces operational overhead, is easier to manage, and is more cost‑effective for a student project. Serverless services also better reflect how many healthcare organizations approach cloud adoption today.

## <ins>Future Improvements</ins>

If I had additional time and unlimited cloud credits, I would expand this system to include predictive chair‑time estimates based on historical patterns and real‑time nurse staffing data. I would also explore tighter integration with scheduling or EHR systems and create role‑specific dashboards for schedulers and nurse managers. These enhancements would further support proactive planning and reduce last‑minute scheduling challenges.

