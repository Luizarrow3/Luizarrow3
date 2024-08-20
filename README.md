@@ -1,6 +1,12 @@
exportar  padrão  {
  clearMocks : verdadeiro ,
  transformar : { } ,
  testEnvironment : "jsdom" ,
  coverageProvider : "v8" ,
  testPathIgnorePatterns : [ "<rootDir>/node_modules/" ,  "<rootDir>/tests/e2e/" ] ,
  modulePathIgnorePatterns : [ "<rootDir>/node_modules/" ,  "<rootDir>/tests/e2e/" ] ,
  coveragePathIgnorePatterns : [
    "<rootDir>/node_modules/" ,
    "<rootDir>/tests/E2E/" ,
  ] ,
