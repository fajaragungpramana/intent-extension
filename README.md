# Android Intent Extension
[![](https://jitpack.io/v/fajaragungpramana/intent-extension.svg)](https://jitpack.io/#fajaragungpramana/intent-extension)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
</br>
</br>
Library for android. Extension to helping navigate between activity or module.

## Installation
Add it in your root build.gradle at the end of repositories:

```gradle
allProjects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```
Add the dependency:
```gradle
dependencies {
	implementation 'com.github.fajaragungpramana:intent-extension:0.0.1'
}
```

## Usage
In activity or fragment.
```kotlin
// <DetailActivity> is the activity purpose.
startActivity<DetailActivity>() // Intent to another activity.

// PathToActivityModuleClass. Example: com.github.fajaragungpramana.detail.DetailActivity
startActivityModule("PathToActivityModuleClass")  // Intent to another activity module.
```

Sending data to purpose.
```kotlin
// <DetailActivity> is the activity purpose.
startActivity<DetailActivity>("key" to "value", "key" to 1) // Key always string, value can be adjusted as desired

startActivityModule("PathToActivityModuleClass", "key" to "value", "key" to 1)  // Key always string, value can be adjusted as desired
```

To receive the data sent
```kotlin
intent.extras?.getString("key")

intent.extras?.getInt("key")
```

## License
Copyright 2021 Fajar Agung Pramana

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
