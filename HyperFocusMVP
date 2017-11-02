package com.example.nestor.hyperfocusmvp;

import android.os.CountDownTimer;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class HyperFocusMVP extends AppCompatActivity {

    EditText editText2;
    Button button2;
    TextView textView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_hyper_focus_mvp);

        editText2 = (EditText) findViewById (R.id.editText2);
        button2 = (Button) findViewById (R.id.button2);
        textView = (TextView) findViewById (R.id.textView);

        button2.setOnClickListener(new View.OnClickListener()  {
            @Override
            public void onClick(View view)  {
                String text = editText2.getText().toString();
                if(!text.equalsIgnoreCase("")) {
                    int seconds = Integer.valueOf(text);
                    int minutes = seconds / 60;
                    seconds = seconds % 60;
                    CountDownTimer countDownTimer = new CountDownTimer(seconds * 1000, 1000) {
                        @Override
                        public void onTick(long millis) {
                            textView.setText(" seconds: " + (int) (millis / 1000));
                        }

                        @Override
                        public void onFinish() {
                            textView.setText("Congratulations! You met your goal!");
                        }

                    }.start();
                }
            }
        });
    }
}
