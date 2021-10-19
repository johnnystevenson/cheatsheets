| Usage  | Description |
| ------------- | ------------- |
| `TEST(group,name){}`  | Defines a test in a group  |
| `TEST_F(fixture,name){}` | Defines a test within a fixture |
| `ASSERT_` | Asserts cause test to fail immediately. Can only be used from within TESTs. All examples given for `EXPECT_` also work with `ASSERT_` |
| `EXPECT_` | Fails test, but continues execution. Can be used within subfunctions |
| `EXPECT_TRUE( cond )` | Expect condition to be true |
| `EXPECT_FALSE( cond )` | Uses ! operator |
| `EXPECT_EQ(expected, actual)` | Uses == operator |
| `EXPECT_NE(expected, actual)` | Uses != operator |
| `EXPECT_STREQ(expected, actual)` | `strcmp` C-strings. Use `EXPECT_EQ` for `std::string` |
| `EXPECT_THROW(call(), ExType)` | Test that call() throws an exception of type ExType |
| `EXPECT_NO_THROW( call() )` | Test that `call()` does not throw. Note that unexpected exceptions or exceptions thrown in `SetUp()` or `TearDown()` do not generate helpful output |
| `EXPECT_NEAR( expected, actual, tolerance )` | Test that a value is within a tolerable range of the expected value |

# Example Test Fixture
```
#include <gtest/gtest.h>

class TestFixture : public ::testing:Test {
 public:
   TestFixture()
   {
      // A new TestFixture is created for each test
   }

   void SetUp()
   {
      // Run prior to each test
   }

   void TearDown()
   {
      // Run after each test, including on failure
   }
}

TEST_F( TestFixture, Test1 )
{
   FAIL( "TODO" );
}
```
