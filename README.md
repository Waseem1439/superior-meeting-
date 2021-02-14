# superior-meeting-
how to make video calling app or how to make meeting like zoom 
 URL ServerURL;
        try {
            ServerURL=new URL("https://meet.jit.si");
            JitsiMeetConferenceOptions options = new JitsiMeetConferenceOptions.Builder()
                    .setServerURL(ServerURL)
                    .setWelcomePageEnabled(false)
                    .build();
            JitsiMeet.setDefaultConferenceOptions(options);
        } catch (MalformedURLException e) {
            e.printStackTrace();
        }

        join.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                JitsiMeetConferenceOptions options=new JitsiMeetConferenceOptions.Builder()
                        .setWelcomePageEnabled(false)
                        .setRoom(code.getText().toString())
                        .build();
                JitsiMeetActivity.launch(DashBoadActivity.this,options);

            }
        });
