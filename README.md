package com.example.basketball;

// Import

import android.view.View;
import android.widget.Button;
import android.widget.ImageView;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity
{
  Button oneA,twoA,threeA;
  Button oneB,twoB,threeB;
  TextView resultA,resultB;
  ImageView resetA,resetB;

    int ResultA = 0;
    int ResultB = 0;
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        call();
    }
    private void call()
    {
        fvById();

        OneA();
        TwoA();
        ThreeA();

        OneB();
        TwoB();
        ThreeB();

        ResetA();
        ResetB();
    }
    public void fvById()
    {
        oneA = findViewById(R.id.increeOneA);
        twoA = findViewById(R.id.increeTwoA);
        threeA = findViewById(R.id.increeThreeA);
        oneB = findViewById(R.id.increeOneB);
        twoB = findViewById(R.id.increeTwoB);
        threeB = findViewById(R.id.increeThreeB);
        resultA = findViewById(R.id.resultA);
        resultB = findViewById(R.id.resultB);
        resetA = findViewById(R.id.resetA);
        resetB = findViewById(R.id.resetB);
    }

    public void OneA()
    {
        oneA.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                ResultA = ResultA + 1;
                resultA.setText(ResultA+"");
            }
        });
    }

    public void TwoA()
    {
        twoA.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                ResultA = ResultA + 2;
                resultA.setText(ResultA+"");
            }
        });
    }

    public void ThreeA()
    {
        threeA.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                ResultA = ResultA + 3;
                resultA.setText(ResultA+"");
            }
        });
    }

    public void OneB()
    {
        oneB.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                ResultB = ResultB + 1;
                resultB.setText(ResultB+"");
            }
        });
    }

    public void TwoB()
    {
        twoB.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                ResultB = ResultB + 2;
                resultB.setText(ResultB+"");
            }
        });
    }

    public void ThreeB()
    {
        threeB.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                ResultB = ResultB + 3;
                resultB.setText(ResultB+"");
            }
        });
    }

    public void ResetA()
    {
        resetA.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                ResultA = 0;
                resultA.setText(ResultA+"");
            }
        });
    }

    public void ResetB()
    {
        resetB.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                ResultB = 0;
                resultB.setText(ResultB+"");
            }
        });
    }
}
