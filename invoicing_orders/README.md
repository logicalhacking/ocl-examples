# InvoicingOrders
A simple invoicing model.

## Data Sheet
* Format:               ArgoUML 0.26
* Language:             UML/OCL

For further information (license, citation, etc.), please look at the [README.md](../)
of the main directory. 

## The InvoicingOrders System
This simple invoicing system is based on the book "Software
Specification Methods: An Overview Using a Case Study" by M. Frappier
and H. Habrias (ISBN 1-85233-353-7). 

The InvoicingOrders system can informally described as follows: 
1. The subject is to InvoicingOrders orders.
2. To InvoicingOrders is to change the state of an order (to change it
   from the state ``pending'' to ``invoiced'').
3. On an order, we have one and one only reference to an ordered
   product of a certain quantity. The quantity can be different to
   other orders.
4. The same reference can be ordered on several different
   orders.
5. The state of the order will be changed into ``invoiced'' if the
   ordered quantity is either less or equal to the quantity which is
   in stock according to the reference of the ordered product.
6. You have to consider the following two cases:
   * **Case 1:** 
     All the ordered references are references in the stock. The
     stock or the set of orders may vary:
     * due to the entry of new orders or canceled orders;
     * due to having a new entry of quantities of products in
       stock at the warehouse.

     But, we do not have to take these entries into account. This
     means that you will not receive two entry flows (orders, entries
     in stock). The stock and the set of orders are always given to
     you in an up-to-date state.
   * **Case 2:**
     You do have to take into account the entries of
     * new orders;
     * cancellations of orders;
     * entries of quantities in the stock.

  
