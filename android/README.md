# expo-android-build-test
reproducible android build issue example

Run:
`npm install && npm run android`

see below build issue
<details><summary> build error </summary>

```
> Task :expo-modules-core:buildCMakeDebug[arm64-v8a] FAILED
C/C++: ninja: Entering directory `/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/android/.cxx/Debug/m5p3ck62/arm64-v8a'
C/C++: ld: error: undefined symbol: operator delete(void*)
C/C++: ld: error: undefined symbol: operator new(unsigned long)
C/C++: ld: error: undefined symbol: __cxa_begin_catch
C/C++: ld: error: undefined symbol: std::terminate()
C/C++: ld: error: undefined symbol: __cxa_allocate_exception
C/C++: ld: error: undefined symbol: typeinfo for std::length_error
C/C++: ld: error: undefined symbol: std::length_error::~length_error()
C/C++: ld: error: undefined symbol: __cxa_throw
C/C++: ld: error: undefined symbol: __cxa_free_exception
C/C++: ld: error: undefined symbol: std::logic_error::logic_error(char const*)
C/C++: ld: error: undefined symbol: vtable for std::length_error
C/C++: ld: error: undefined symbol: std::__ndk1::__vector_base_common<true>::__throw_length_error() const
C/C++: ld: error: undefined symbol: __gxx_personality_v0
C/C++: ld: error: undefined symbol: std::__ndk1::__shared_weak_count::__release_weak()
C/C++: ld: error: undefined symbol: std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >::compare(unsigned long, unsigned long, char const*, unsigned long) const
C/C++: ld: error: undefined symbol: std::exception::~exception()
C/C++: ld: error: undefined symbol: vtable for __cxxabiv1::__si_class_type_info
C/C++: ld: error: undefined symbol: typeinfo for std::exception
C/C++: ld: error: undefined symbol: std::exception::what() const
C/C++: ld: error: undefined symbol: std::runtime_error::runtime_error(char const*)
C/C++: ld: error: too many errors emitted, stopping now (use -error-limit=0 to see all errors)
C/C++: clang++: error: linker command failed with exit code 1 (use -v to see invocation)

FAILURE: Build completed with 2 failures.

1: Task failed with an exception.
-----------
* What went wrong:
Execution failed for task ':expo-modules-core:buildCMakeDebug[arm64-v8a]'.
> com.android.ide.common.process.ProcessException: ninja: Entering directory `/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/android/.cxx/Debug/m5p3ck62/arm64-v8a'
  [1/1] Linking CXX shared library ../../../../build/intermediates/cxx/Debug/m5p3ck62/obj/arm64-v8a/libexpo-modules-core.so
  FAILED: ../../../../build/intermediates/cxx/Debug/m5p3ck62/obj/arm64-v8a/libexpo-modules-core.so 
  : && /Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/bin/clang++ --target=aarch64-none-linux-android21 --sysroot=/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot -fPIC -DANDROID -fdata-sections -ffunction-sections -funwind-tables -fstack-protector-strong -no-canonical-prefixes -D_FORTIFY_SOURCE=2 -Wformat -Werror=format-security -fexceptions -frtti -stdlib=libc++ -DREACT_NATIVE_TARGET_VERSION=71 -g  -fno-limit-debug-info  -Wl,--build-id=sha1 -Wl,--no-rosegment -Wl,--fatal-warnings -Qunused-arguments -Wl,--no-undefined -shared -Wl,-soname,libexpo-modules-core.so -o ../../../../build/intermediates/cxx/Debug/m5p3ck62/obj/arm64-v8a/libexpo-modules-core.so CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/Exceptions.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/ExpoModulesHostObject.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JNIFunctionBody.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JNIInjector.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JSIInteropModuleRegistry.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JSReferencesCache.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaCallback.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaReferencesCache.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaScriptModuleObject.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaScriptObject.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaScriptRuntime.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaScriptTypedArray.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaScriptValue.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/MethodMetadata.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/WeakRuntimeHolder.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/types/AnyType.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/types/ExpectedType.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/types/FrontendConverter.cpp.o CMakeFiles/expo-modules-core.dir/src/main/cpp/types/FrontendConverterProvider.cpp.o  /Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/lib/aarch64-linux-android/21/liblog.so  /Users/matthewparavati/.gradle/caches/transforms-3/839e63e695132860efbc878bf673a792/transformed/jetified-fbjni-0.3.0/prefab/modules/fbjni/libs/android.arm64-v8a/libfbjni.so  /Users/matthewparavati/.gradle/caches/transforms-3/80bcec10edf7b36a7acc4848e4b58fa9/transformed/jetified-react-android-0.71.6-debug/prefab/modules/jsi/libs/android.arm64-v8a/libjsi.so  /Users/matthewparavati/.gradle/caches/transforms-3/80bcec10edf7b36a7acc4848e4b58fa9/transformed/jetified-react-android-0.71.6-debug/prefab/modules/reactnativejni/libs/android.arm64-v8a/libreactnativejni.so  /Users/matthewparavati/.gradle/caches/transforms-3/80bcec10edf7b36a7acc4848e4b58fa9/transformed/jetified-react-android-0.71.6-debug/prefab/modules/folly_runtime/libs/android.arm64-v8a/libfolly_runtime.so  /Users/matthewparavati/.gradle/caches/transforms-3/80bcec10edf7b36a7acc4848e4b58fa9/transformed/jetified-react-android-0.71.6-debug/prefab/modules/react_nativemodule_core/libs/android.arm64-v8a/libreact_nativemodule_core.so  -landroid   -latomic -lm && :
  ld: error: undefined symbol: operator delete(void*)
  >>> referenced by new:334 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/new:334)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(expo::jsiArrayToPropNameIdsVector(facebook::jsi::Runtime&, facebook::jsi::Array const&))
  >>> referenced by new:334 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/new:334)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::__ndk1::vector<facebook::jsi::PropNameID, std::__ndk1::allocator<facebook::jsi::PropNameID> >::reserve(unsigned long))
  >>> referenced by new:334 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/new:334)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(void std::__ndk1::vector<facebook::jsi::PropNameID, std::__ndk1::allocator<facebook::jsi::PropNameID> >::__push_back_slow_path<facebook::jsi::PropNameID>(facebook::jsi::PropNameID&&))
  >>> referenced 638 more times
  
  ld: error: undefined symbol: operator new(unsigned long)
  >>> referenced by new:253 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/new:253)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::__ndk1::vector<facebook::jsi::PropNameID, std::__ndk1::allocator<facebook::jsi::PropNameID> >::reserve(unsigned long))
  >>> referenced by new:253 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/new:253)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(void std::__ndk1::vector<facebook::jsi::PropNameID, std::__ndk1::allocator<facebook::jsi::PropNameID> >::__push_back_slow_path<facebook::jsi::PropNameID>(facebook::jsi::PropNameID&&))
  >>> referenced by new:253 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/new:253)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp.o:(std::__ndk1::pair<std::__ndk1::__hash_iterator<std::__ndk1::__hash_node<std::__ndk1::__hash_value_type<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, expo::TypedArrayKind>, void*>*>, bool> std::__ndk1::__hash_table<std::__ndk1::__hash_value_type<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, expo::TypedArrayKind>, std::__ndk1::__unordered_map_hasher<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, std::__ndk1::__hash_value_type<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, expo::TypedArrayKind>, std::__ndk1::hash<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> > >, true>, std::__ndk1::__unordered_map_equal<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, std::__ndk1::__hash_value_type<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, expo::TypedArrayKind>, std::__ndk1::equal_to<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> > >, true>, std::__ndk1::allocator<std::__ndk1::__hash_value_type<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, expo::TypedArrayKind> > >::__emplace_unique_key_args<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, std::__ndk1::pair<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> > const, expo::TypedArrayKind> const&>(std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> > const&, std::__ndk1::pair<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> > const, expo::TypedArrayKind> const&))
  >>> referenced 145 more times
  
  ld: error: undefined symbol: __cxa_begin_catch
  >>> referenced by JSIUtils.cpp
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(__clang_call_terminate)
  >>> referenced by Registration-inl.h:91 (/Users/matthewparavati/.gradle/caches/transforms-3/839e63e695132860efbc878bf673a792/transformed/jetified-fbjni-0.3.0/prefab/modules/fbjni/include/fbjni/detail/Registration-inl.h:91)
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/JSIInteropModuleRegistry.cpp.o:(facebook::jni::detail::FunctionWrapper<facebook::jni::basic_strong_ref<facebook::jni::detail::JTypeFor<facebook::jni::detail::HybridData, facebook::jni::JObject, void>::_javaobject*, facebook::jni::LocalReferenceAllocator> (*)(facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<expo::JSIInteropModuleRegistry, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*>), facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<expo::JSIInteropModuleRegistry, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*, facebook::jni::basic_strong_ref<facebook::jni::detail::JTypeFor<facebook::jni::detail::HybridData, facebook::jni::JObject, void>::_javaobject*, facebook::jni::LocalReferenceAllocator> >::call(_JNIEnv*, _jobject*, facebook::jni::basic_strong_ref<facebook::jni::detail::JTypeFor<facebook::jni::detail::HybridData, facebook::jni::JObject, void>::_javaobject*, facebook::jni::LocalReferenceAllocator> (*)(facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<expo::JSIInteropModuleRegistry, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*>)))
  >>> referenced by Registration-inl.h:91 (/Users/matthewparavati/.gradle/caches/transforms-3/839e63e695132860efbc878bf673a792/transformed/jetified-fbjni-0.3.0/prefab/modules/fbjni/include/fbjni/detail/Registration-inl.h:91)
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/JSIInteropModuleRegistry.cpp.o:(facebook::jni::detail::FunctionWrapper<void (*)(facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<expo::JSIInteropModuleRegistry, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*>, long&&, facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<facebook::react::CallInvokerHolder, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*>&&, facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<facebook::react::CallInvokerHolder, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*>&&), facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<expo::JSIInteropModuleRegistry, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*, void, long, facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<facebook::react::CallInvokerHolder, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*>, facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<facebook::react::CallInvokerHolder, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*> >::call(_JNIEnv*, _jobject*, long, facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<facebook::react::CallInvokerHolder, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*, facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<facebook::react::CallInvokerHolder, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*, void (*)(facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<expo::JSIInteropModuleRegistry, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*>, long&&, facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<facebook::react::CallInvokerHolder, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*>&&, facebook::jni::alias_ref<facebook::jni::detail::JTypeFor<facebook::jni::HybridClass<facebook::react::CallInvokerHolder, facebook::jni::detail::BaseHybridClass>::JavaPart, facebook::jni::JObject, void>::_javaobject*>&&)))
  >>> referenced 120 more times
  
  ld: error: undefined symbol: std::terminate()
  >>> referenced by JSIUtils.cpp
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(__clang_call_terminate)
  
  ld: error: undefined symbol: __cxa_allocate_exception
  >>> referenced by stdexcept:258 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:258)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::__ndk1::__throw_length_error(char const*))
  >>> referenced by functional:1435 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/functional:1435)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(std::__ndk1::__throw_bad_function_call())
  >>> referenced by TypedArray.cpp:50 (/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp:50)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp.o:(expo::TypedArray::getBuffer(facebook::jsi::Runtime&) const)
  >>> referenced 34 more times
  
  ld: error: undefined symbol: typeinfo for std::length_error
  >>> referenced by stdexcept:258 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:258)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::__ndk1::__throw_length_error(char const*))
  >>> referenced by stdexcept:258 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:258)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::__ndk1::__throw_length_error(char const*))
  
  ld: error: undefined symbol: std::length_error::~length_error()
  >>> referenced by stdexcept:258 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:258)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::__ndk1::__throw_length_error(char const*))
  >>> referenced by stdexcept:258 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:258)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::__ndk1::__throw_length_error(char const*))
  
  ld: error: undefined symbol: __cxa_throw
  >>> referenced by stdexcept:258 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:258)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::__ndk1::__throw_length_error(char const*))
  >>> referenced by functional:1435 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/functional:1435)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(std::__ndk1::__throw_bad_function_call())
  >>> referenced by TypedArray.cpp:50 (/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp:50)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp.o:(expo::TypedArray::getBuffer(facebook::jsi::Runtime&) const)
  >>> referenced 34 more times
  
  ld: error: undefined symbol: __cxa_free_exception
  >>> referenced by stdexcept:258 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:258)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::__ndk1::__throw_length_error(char const*))
  >>> referenced by TypedArray.cpp:50 (/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp:50)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp.o:(expo::TypedArray::getBuffer(facebook::jsi::Runtime&) const)
  >>> referenced by stdexcept:269 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:269)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp.o:(std::__ndk1::__throw_out_of_range(char const*))
  >>> referenced 12 more times
  
  ld: error: undefined symbol: std::logic_error::logic_error(char const*)
  >>> referenced by stdexcept:155 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:155)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::length_error::length_error(char const*))
  >>> referenced by stdexcept:167 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:167)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp.o:(std::out_of_range::out_of_range(char const*))
  >>> referenced by stdexcept:142 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:142)
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/MethodMetadata.cpp.o:(std::invalid_argument::invalid_argument(char const*))
  
  ld: error: undefined symbol: vtable for std::length_error
  >>> referenced by stdexcept:155 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:155)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::length_error::length_error(char const*))
  >>> referenced by stdexcept:155 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/stdexcept:155)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(std::length_error::length_error(char const*))
  >>> the vtable symbol may be undefined because the class is missing its key function (see https://lld.llvm.org/missingkeyfunction)
  
  ld: error: undefined symbol: std::__ndk1::__vector_base_common<true>::__throw_length_error() const
  >>> referenced by vector:1027 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/vector:1027)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(void std::__ndk1::vector<facebook::jsi::PropNameID, std::__ndk1::allocator<facebook::jsi::PropNameID> >::__push_back_slow_path<facebook::jsi::PropNameID>(facebook::jsi::PropNameID&&))
  >>> referenced by vector:993 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/vector:993)
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaReferencesCache.cpp.o:(std::__ndk1::vector<std::__ndk1::pair<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> > >, std::__ndk1::allocator<std::__ndk1::pair<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> > > > >::vector(std::initializer_list<std::__ndk1::pair<std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >, std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> > > >))
  >>> referenced by vector:1027 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/vector:1027)
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaScriptModuleObject.cpp.o:(void std::__ndk1::vector<std::__ndk1::unique_ptr<expo::AnyType, std::__ndk1::default_delete<expo::AnyType> >, std::__ndk1::allocator<std::__ndk1::unique_ptr<expo::AnyType, std::__ndk1::default_delete<expo::AnyType> > > >::__push_back_slow_path<std::__ndk1::unique_ptr<expo::AnyType, std::__ndk1::default_delete<expo::AnyType> > >(std::__ndk1::unique_ptr<expo::AnyType, std::__ndk1::default_delete<expo::AnyType> >&&))
  >>> referenced 10 more times
  
  ld: error: undefined symbol: __gxx_personality_v0
  >>> referenced by JSIUtils.cpp
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/JSIUtils.cpp.o:(DW.ref.__gxx_personality_v0)
  
  ld: error: undefined symbol: std::__ndk1::__shared_weak_count::__release_weak()
  >>> referenced by memory:3549 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/memory:3549)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(expo::LazyObject::~LazyObject())
  >>> referenced by memory:3549 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/memory:3549)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(expo::LazyObject::~LazyObject())
  >>> referenced by memory:3549 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/memory:3549)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(expo::LazyObject::get(facebook::jsi::Runtime&, facebook::jsi::PropNameID const&))
  >>> referenced 359 more times
  
  ld: error: undefined symbol: std::__ndk1::basic_string<char, std::__ndk1::char_traits<char>, std::__ndk1::allocator<char> >::compare(unsigned long, unsigned long, char const*, unsigned long) const
  >>> referenced by string:3996 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/string:3996)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(expo::LazyObject::get(facebook::jsi::Runtime&, facebook::jsi::PropNameID const&))
  
  ld: error: undefined symbol: std::exception::~exception()
  >>> referenced by functional:1435 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/functional:1435)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(std::__ndk1::__throw_bad_function_call())
  >>> referenced by functional:1435 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/functional:1435)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(std::__ndk1::__throw_bad_function_call())
  >>> referenced by functional:1420 (/Users/matthewparavati/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/sysroot/usr/include/c++/v1/functional:1420)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(std::__ndk1::bad_function_call::~bad_function_call())
  >>> referenced 1 more times
  
  ld: error: undefined symbol: vtable for __cxxabiv1::__si_class_type_info
  >>> referenced by LazyObject.cpp
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(typeinfo for expo::LazyObject)
  >>> referenced by LazyObject.cpp
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(typeinfo for std::__ndk1::bad_function_call)
  >>> referenced by ExpoModulesHostObject.cpp
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/ExpoModulesHostObject.cpp.o:(typeinfo for expo::ExpoModulesHostObject)
  >>> referenced 68 more times
  >>> the vtable symbol may be undefined because the class is missing its key function (see https://lld.llvm.org/missingkeyfunction)
  
  ld: error: undefined symbol: typeinfo for std::exception
  >>> referenced by LazyObject.cpp
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(typeinfo for std::__ndk1::bad_function_call)
  >>> referenced by JSIInteropModuleRegistry.cpp
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/JSIInteropModuleRegistry.cpp.o:(.data+0x0)
  >>> referenced by JavaCallback.cpp
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/JavaCallback.cpp.o:(.data+0x0)
  >>> referenced 4 more times
  
  ld: error: undefined symbol: std::exception::what() const
  >>> referenced by LazyObject.cpp
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/LazyObject.cpp.o:(vtable for std::__ndk1::bad_function_call)
  
  ld: error: undefined symbol: std::runtime_error::runtime_error(char const*)
  >>> referenced by TypedArray.cpp:50 (/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp:50)
  >>>               CMakeFiles/expo-modules-core.dir/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/common/cpp/TypedArray.cpp.o:(expo::TypedArray::getBuffer(facebook::jsi::Runtime&) const)
  >>> referenced by Exceptions.cpp:103 (/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/android/src/main/cpp/Exceptions.cpp:103)
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/Exceptions.cpp.o:(expo::throwPendingJniExceptionAsCppException())
  >>> referenced by MethodMetadata.cpp:36 (/Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/android/src/main/cpp/MethodMetadata.cpp:36)
  >>>               CMakeFiles/expo-modules-core.dir/src/main/cpp/MethodMetadata.cpp.o:(expo::createJavaCallbackFromJSIFunction(facebook::jsi::Function&&, std::__ndk1::weak_ptr<facebook::react::LongLivedObjectCollection>, facebook::jsi::Runtime&, expo::JSIInteropModuleRegistry*, bool))
  >>> referenced 1 more times
  
  ld: error: too many errors emitted, stopping now (use -error-limit=0 to see all errors)
  clang++: error: linker command failed with exit code 1 (use -v to see invocation)
  ninja: build stopped: subcommand failed.
  
  C++ build system [build] failed while executing:
      /Users/matthewparavati/Library/Android/sdk/cmake/3.22.1/bin/ninja \
        -C \
        /Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/android/.cxx/Debug/m5p3ck62/arm64-v8a \
        expo-modules-core
    from /Users/matthewparavati/Code/android-build-test/node_modules/expo-modules-core/android

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.
==============================================================================

2: Task failed with an exception.
-----------
* What went wrong:
java.lang.StackOverflowError (no error message)

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.
==============================================================================

* Get more help at https://help.gradle.org

Deprecated Gradle features were used in this build, making it incompatible with Gradle 8.0.

You can use '--warning-mode all' to show the individual deprecation warnings and determine if they come from your own scripts or plugins.

See https://docs.gradle.org/7.5.1/userguide/command_line_interface.html#sec:command_line_warnings

Execution optimizations have been disabled for 1 invalid unit(s) of work during this build to ensure correctness.
Please consult deprecation warnings for more details.

BUILD FAILED in 14s
184 actionable tasks: 7 executed, 177 up-to-date
Error: /Users/matthewparavati/Code/android-build-test/android/gradlew exited with non-zero code: 1
Error: /Users/matthewparavati/Code/android-build-test/android/gradlew exited with non-zero code: 1
    at ChildProcess.completionListener (/Users/matthewparavati/Code/android-build-test/node_modules/@expo/spawn-async/build/spawnAsync.js:52:23)
    at Object.onceWrapper (node:events:628:26)
    at ChildProcess.emit (node:events:513:28)
    at maybeClose (node:internal/child_process:1100:16)
    at Process.ChildProcess._handle.onexit (node:internal/child_process:304:5)
    ...
    at Object.spawnAsync [as default] (/Users/matthewparavati/Code/android-build-test/node_modules/@expo/spawn-async/build/spawnAsync.js:17:21)
    at spawnGradleAsync (/Users/matthewparavati/Code/android-build-test/node_modules/@expo/cli/build/src/start/platforms/android/gradle.js:72:46)
    at Object.assembleAsync (/Users/matthewparavati/Code/android-build-test/node_modules/@expo/cli/build/src/start/platforms/android/gradle.js:52:18)
    at runAndroidAsync (/Users/matthewparavati/Code/android-build-test/node_modules/@expo/cli/build/src/run/android/runAndroidAsync.js:31:24)
```

</details>

See comment in `android/build.gradle` but I've found that if I change the `ndkVersion` to `24.0.8215888` then the build works. I'm not really sure why and changing that was a complete long shot to try and solve this issue that's been blocking me for a day.