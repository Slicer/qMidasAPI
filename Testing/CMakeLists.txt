INCLUDE_DIRECTORIES(
  ${qMidasAPI_SOURCE_DIR}
  )

CREATE_TEST_SOURCELIST(Tests 
  qMidasAPICppTests.cpp
  qMidasAPITest.cpp
  )
SET(TestsToRun ${Tests})
REMOVE(TestsToRun qMidasAPICppTests.cpp)

ADD_DEFINITIONS(-D_CRT_SECURE_NO_DEPRECATE)

ADD_EXECUTABLE(qMidasAPICppTests ${Tests})
TARGET_LINK_LIBRARIES(qMidasAPICppTests qMidasAPI)

MACRO(SIMPLE_TEST TESTNAME)
  ADD_TEST(NAME ${TESTNAME} COMMAND qMidasAPICppTests ${TESTNAME})
ENDMACRO()

SIMPLE_TEST(qMidasAPITest)
