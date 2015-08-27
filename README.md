# Shelly
Simple sharing for Android.

This library wraps sharing intents with a clean and simple to understand interface for a number of specific use-cases.

## Sample usage
See the sample project in the `sample/` folder.

## Installation

Add this into your build.gradle to get the Shelly goodness.

```
repositories {
    maven {
        url "http://dl.bintray.com/jtribe/maven"
    }
}

dependencies {
    compile 'au.com.jtribe.shelly:shelly:0.1'
}

```

### Sharing Generic Information

Sharing some text and an image:
```java
Shelly.share(context)
  .text("text with image")
  .image(myImageUri)
  .send();
```

Sharing some text and a video:
```java
Shelly.share(context)
  .text("text with video")
  .video(myVideoUri)
  .send();
```

### Sending Emails
Sending an email to someone:
```java
Shelly.email(context)
  .to("angus@jtribe.com")
  .subject("Subject Text")
  .body("Email Body")
  .send();
```

 Sending an email to multiple people at once:
 ```java
Shelly.email(context)
  .to("angus@jtribe.com")
  .to("mark@jtribe.com")
  .to("another@email.com")
  .to("yetanother@email.com")
  .subject("Subject Text")
  .body("Email Body")
  .send();
 ```

## Issues and Feedback
Please use [Github Issues](https://github.com/jtribe/shelly/issues "Github Issues") for feature requests or bug reports.

## License
Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
