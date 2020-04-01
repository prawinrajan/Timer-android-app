# Timer-android-app
Simple Timer android App for basic purpose 

Main Funationality of the egg timer app depends on the following code,<Br/>

## code

public void updateTimer(int secondsLeft){
        int minutes =(int)secondsLeft/60;
        int seconds =  secondsLeft - minutes*60;
        String secondString =Integer.toString(seconds);
        if (seconds<=9){
            secondString="0"+secondString;
        }
         timerTextview.setText(Integer.toString(minutes)+":"+secondString);

}

## code 

countDownTimer = new CountDownTimer(timerSeekbar.getProgress() * 1000 + 100, 1000) {
                @Override
                public void onTick(long millisUntilFinished) {
                    updateTimer((int) millisUntilFinished / 1000);
                }
                
### Reference
I am going to explain what is what , I give the link to read official android docu. 
Click Here,<br/> https://developer.android.com/reference/android/os/CountDownTimer

#### output
<img src="https://github.com/prawinrajan/Timer-android-app/blob/master/Screenshot_20200401-115826.png" width="250" height="450" />
