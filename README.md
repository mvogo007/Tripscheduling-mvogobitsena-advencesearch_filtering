# Tripscheduling-mvogobitsena-advencesearch_filtering
LinearLayout < android {

    buildFeatures {
        viewBinding true
    }
}

        < !--res / layout / item_trip.xml-- xmlns:android="http://schemas.android.com/apk/res/android"-->
android;orientation="vertical"
android:padding="16dp"
android:layout_width="match_parent"


        TextView
android:b
android:id="@+id/text_destination"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Destination"
android:textSize="16sp"

        TextView
android:id="@+id/text_status"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Status"
android:textSize="14sp"

        TextView
android:id="@+id/text_budget"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Budget"
android:textSize="14sp"

        TextView
android:id="@+id/text_travelers"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Travelers"
android:textSize="14sp"

        <TextView
android:id="@+id/text_dates"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Dates"
android:textSize="14sp"
        </LinearLayout>
)
/$
data_class Trip(
        val destination: String,
                val status: String,
        val budget: Double,
        val travelers: Int,
val dates: String
)

private class TripAdapter <Trip>
private class tripListList <Trip>
private class onTripClick



Boolean b = RecyclerView.Adapter >= TripAdapter.TripViewHolder>


RecyclerView.Adapter >= TripAdapter.TripViewHolder>


class TripFragment

def var = Fragment(R.layout.fragment_trip) {

   private lateinit var_recyclerView; RecyclerView
   private lateinit var_tripList; List<Trip>

   override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
       super.onViewCreated(view, savedInstanceState)

       // Sample data
       tripList = listOf(
               Trip("Paris", "Planned", 1500.0, 2, "2023-07-15 to 2023-07-22"),
               Trip("Tokyo", "Completed", 2000.0, 3, "2023-06-01 to 2023-06-10"),
               Trip("New York", "Planned", 1800.0, 4, "2023-08-05 to 2023-08-12")
       )

       recyclerView = view.findViewById(R.id.recyclerView)

       // Initialize the adapter
       val adapter = TripAdapter(
               tripList = tripList,
               onTripClick = { trip ->
                   // Handle item click
                   Toast.makeText(context, "Clicked: ${trip.destination}", Toast.LENGTH_SHORT).show()
               },
               onTripLongClick = { trip ->
                   // Handle long press
                   Toast.makeText(context, "Long clicked: ${trip.destination}", Toast.LENGTH_SHORT).show()
               }
       )

       // Set up the RecyclerView
       recyclerView.adapter = adapter
       recyclerView.layoutManager = LinearLayoutManager(context)
   }
}


       <!-- res/layout/fragment_trip.xml -->
       LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
android:orientation="vertical"
android:layout_width="match_parent"
android:layout_height="match_parent">

        RecyclerView
android:id="@+id/recyclerView"
android:layout_width="match_parent"
android:layout_height="match_parent"
/LinearLayout>
