package com.example.bingcab;

import android.app.Activity;
import android.content.Intent;
import android.media.MediaPlayer;
import android.os.Bundle;

public class StartScreen extends Activity {
> Thread logoTimer;
> > @Override
> > public void onCreate(Bundle savedInstanceState) {
> > > super.onCreate(savedInstanceState);
> > > setContentView(R.layout.splashscreen);


/**AsyncTask<Object, Object, Object> saveContactTask =

> new AsyncTask<Object, Object, Object>()
> {
> > @Override
> > protected Object doInBackground(Object... params)
> > {

> //        saveContact(); // save contact to the database
> > return null;
> > } // end method doInBackground**


> @Override
> protected void onPostExecute(Object result)
> {
> > Toast.makeText(SplashActivity.this, "done",Toast.LENGTH\_SHORT).show();
> > > //finish();

> > // return to the previous Activity

> } // end method onPostExecute
> }; // end AsyncTask

> // save the contact to the database using a separate thread
> saveContactTask.execute((Object[.md](.md)) null); **/**


> logoTimer = new Thread() {
> > public void run() {
> > > try {
> > > > sleep(5000);
> > > > Intent menuIntent = new Intent(StartScreen.this,AgreeTermsActivity.class);
> > > > startActivity(menuIntent);


> } catch (InterruptedException e) {
> > // TODO Auto-generated catch block
> > e.printStackTrace();

> } finally {
> > finish();

> }
> }
> };
> try {
> > logoTimer.start();

> } catch (Exception e) {
> > // TODO Auto-generated catch block
> > e.printStackTrace();

> }




> }



> @Override
> protected void onPause() {
> > // TODO Auto-generated method stub
> > super.onPause();
> > logoTimer=null;



> }
> @Override
> protected void onStop() {
> > // TODO Auto-generated method stub
> > super.onStop();
> > logoTimer=null;



> }
> > @Override
> > > protected void onDestroy() {
> > > > super.onDestroy();
> > > > logoTimer=null;


> }

}