# Introduction

CITYSPORTS treadmills rely on the EQiSports app, which is objectively terrible.

Here are some reasons why:

- Can't pause and resume workouts
- Doesn't record workout history
- Won't push data to Apple Health
- Basically just a tech demo of the integration

This project aims to reverse engineer the bluetooth protocol used by these treadmills and then to create a better app that addresses these concerns.

# Protocol

The details of the protocol are [here](protocol).

And this is a proof of concept.

After reverse engineering the protocol, I discovered that the treadmill broadly conforms to the Bluetooth Low Energy Fitness Machine Profile Specification. As such, extending the capabilities of the application has become a lot easier. For instance pausing and resuming a workout, which is not possible with the EQiSports app, is actually supported by the hardware. 

# Proof of Concept

It is truly barebones and not good code, but it works and should be reasonably easy to understand.

This is a MAUI app and should be fairly straightforward to build.

1. Open the directory with the csproj file in
2. Run `dotnet build`
3. Install the app on your phone

I'm not including instructions on how to configure iOS or Android toolchains... Sorry but Google is your friend.