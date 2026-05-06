# ---------------------------
# 7B. Additional hypothesis-based analyses
# ---------------------------

# H2: Safety-net receipt and employment improvement
tab_h2 <- table(df$safety_net_binary, df$employment_improved)

h2_test <- fisher.test(tab_h2)

h2_summary <- df %>%
  count(safety_net_binary, employment_improved) %>%
  group_by(safety_net_binary) %>%
  mutate(percent = round(100 * n / sum(n), 1)) %>%
  ungroup()

cat("\nH2: Safety-net receipt and employment improvement\n")
print(tab_h2)
print(h2_test)
print(h2_summary)


# H3: Duration since migration and income after migration
h3_spearman <- cor.test(
  df$years_staying_in_dhaka,
  df$income_after,
  method = "spearman",
  use = "complete.obs"
)

h3_kruskal <- kruskal.test(income_after ~ duration_group, data = df)

h3_summary <- df %>%
  group_by(duration_group) %>%
  summarise(
    n = n(),
    median_income = median(income_after, na.rm = TRUE),
    mean_income = mean(income_after, na.rm = TRUE),
    .groups = "drop"
  )

cat("\nH3: Duration since migration and post-migration income\n")
print(h3_spearman)
print(h3_kruskal)
print(h3_summary)


# H4: Education and hygiene practices
tab_h4_kitchen <- table(df$edu_group, df$kitchen_clean)
tab_h4_wash <- table(df$edu_group, df$wash_before_eating)

h4_kitchen_test <- fisher.test(tab_h4_kitchen)
h4_wash_test <- fisher.test(tab_h4_wash)

h4_kitchen_summary <- df %>%
  count(edu_group, kitchen_clean) %>%
  group_by(edu_group) %>%
  mutate(percent = round(100 * n / sum(n), 1)) %>%
  ungroup()

h4_wash_summary <- df %>%
  count(edu_group, wash_before_eating) %>%
  group_by(edu_group) %>%
  mutate(percent = round(100 * n / sum(n), 1)) %>%
  ungroup()

cat("\nH4: Education and hygiene practices\n")
print(tab_h4_kitchen)
print(h4_kitchen_test)
print(h4_kitchen_summary)

print(tab_h4_wash)
print(h4_wash_test)
print(h4_wash_summary)


# H5: Displacement type and health/income outcomes
tab_h5_health <- table(df$displacement_group, df$self_health)

h5_health_test <- fisher.test(tab_h5_health)
h5_income_test <- kruskal.test(income_after ~ displacement_group, data = df)

h5_income_summary <- df %>%
  group_by(displacement_group) %>%
  summarise(
    n = n(),
    median_income = median(income_after, na.rm = TRUE),
    mean_income = mean(income_after, na.rm = TRUE),
    .groups = "drop"
  )

cat("\nH5: Displacement type and health/income outcomes\n")
print(tab_h5_health)
print(h5_health_test)
print(h5_income_test)
print(h5_income_summary)


# H6: Safety-net receipt and income/health outcomes
h6_income_test <- wilcox.test(income_after ~ safety_net_binary, data = df)

tab_h6_health <- table(df$safety_net_binary, df$self_health)
h6_health_test <- fisher.test(tab_h6_health)

h6_income_summary <- df %>%
  group_by(safety_net_binary) %>%
  summarise(
    n = n(),
    median_income = median(income_after, na.rm = TRUE),
    mean_income = mean(income_after, na.rm = TRUE),
    .groups = "drop"
  )

cat("\nH6: Safety-net receipt and income/health outcomes\n")
print(h6_income_test)
print(tab_h6_health)
print(h6_health_test)
print(h6_income_summary)
