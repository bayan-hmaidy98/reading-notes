# Create dynamic lists with RecyclerView

When it coms to display large numer of data, `RecyclerView` would make it an easy job because it would create te elements **dynamically.** The main point of `RecyclerView` that it can reuse the view instead of destroing it. This leads to improve the performance ofthe app and resuce its consumption of battery. 

Let's have a tour in related **Key classes:**

## Key classes
1. `RecyclerView:` contains many views related to data. 
2. `ViewHolder:` No data is assocated to it. Once it's created, the `RecyclerView` binds its data to it. 
3. `Adapter:` it is used to call the method inside it and link the views to their *data*.
4. `LayoutManager:` Here you have the choise to use one of the defined layout in the `RecyclerView` library, or use one of your choise. 

## How to implement `RecyclerView` ?

1. Determine the grid layout. 
2. Decide hte behaviour of each element in the list. To do so, you'll need the `ViewHolder` because as we have mntioned earlier , it's used to determine the functionality of the `RecyclerView`.
3. Determine tour `Adapter.`

Let's dig deep in the first step.. 

## Plan your layout

`LayoutManager` class is usd to arrange the items in `RecyclerView`. We can 3 layouts managers dpending on the dimensions: 

1. `LinearLayoutManager`: arrange items in one-dimentional list. 
2. 'GridLayoutManager' : arrange items in 2-dimentional grid.
3. `StaggeredGridLayoutManager is similar to GridLayoutManager, but it does not require that items in a row have the same height (for vertical grids) or items in the same column have the same width (for horizontal grids). The result is that the items in a row or column can end up offset from each other.`

## Implementing your adapter and view holder

Key methods used to define the adapter: 

1. `onCreateViewHolder()`
2. `onBindViewHolder()`
3. `getItemCount`