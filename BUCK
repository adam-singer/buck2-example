# A list of available rules and their signatures can be found here: https://buck2.build/docs/api/rules/

genrule(
    name = "hello_world",
    out = "out.txt",
    cmd = "echo ${PWD} > $OUT",
)


genrule(
    name = "test_sh",
    out = "test.sh",
    cmd =  """
      echo whoami > $OUT;
      echo echo ${PWD} >> $OUT;
      echo ls -al >> $OUT;
      echo 'find . -type f -exec ls -l {} \\;' >> $OUT;
      chmod +x $OUT
      """
)

sh_binary(
    name = "test_bin", 
    main = "//:test_sh",
)