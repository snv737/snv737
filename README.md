 public class MainActivity extends AppCompatActivity {
private Button move;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
move=findViewById(R. id.Move);
move.setOnClickListener (new View.OnClickListener){
goverride
public void onClick(View v) {
Intent intent=new Intent( packageContext: MainActivity.this,second.class);
startActivity(intent);
