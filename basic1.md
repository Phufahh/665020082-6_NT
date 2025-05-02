basicR
================
Nanthanit
2025-05-02

``` r
1 + 1
```

    ## [1] 2

``` r
2 * 2
```

    ## [1] 4

``` r
2/2
```

    ## [1] 1

``` r
plant_height <- 10.5
leaf_count <- 25
```

``` r
total_height <- plant_height <- 10.5*2
```

``` r
plant_height <- c(10.5, 20.5, 12.5, 8.5)
plant_height*10
```

    ## [1] 105 205 125  85

``` r
plant_height*leaf_count
```

    ## [1] 262.5 512.5 312.5 212.5

``` r
plant_height_2 <- c(200,300,500,1000)
plant_height * plant_height_2
```

    ## [1] 2100 6150 6250 8500

``` r
plant_height_2 <-plant_height_2 + 1000
plant_height_2
```

    ## [1] 1200 1300 1500 2000

``` r
weight <- 2.5
class(weight)
```

    ## [1] "numeric"

``` r
count <- 10L 
count
```

    ## [1] 10

``` r
class(count)
```

    ## [1] "integer"

``` r
count+10
```

    ## [1] 20

``` r
count <- "10L"
class (count)
```

    ## [1] "character"

``` r
is_flowering <- "TRUE"
class(is_flowering)
```

    ## [1] "character"

``` r
heights <- c(10.2, 15.7, 12.3, 9.8, 11.5)
heights
```

    ## [1] 10.2 15.7 12.3  9.8 11.5

``` r
species <- c("Arabidopsis", "Nicotiana", "Oryza", "Zea", "Solanum")
species
```

    ## [1] "Arabidopsis" "Nicotiana"   "Oryza"       "Zea"         "Solanum"

``` r
heights
```

    ## [1] 10.2 15.7 12.3  9.8 11.5

``` r
heights [3]
```

    ## [1] 12.3

``` r
heights [2:4]
```

    ## [1] 15.7 12.3  9.8

``` r
heights [c (2,4) ]
```

    ## [1] 15.7  9.8

``` r
heights [-c (2,4) ]
```

    ## [1] 10.2 12.3 11.5

``` r
species
```

    ## [1] "Arabidopsis" "Nicotiana"   "Oryza"       "Zea"         "Solanum"

``` r
species [3]
```

    ## [1] "Oryza"

``` r
species [2:4]
```

    ## [1] "Nicotiana" "Oryza"     "Zea"

``` r
species [c (2,4) ]
```

    ## [1] "Nicotiana" "Zea"

``` r
species [-c (2,4) ]
```

    ## [1] "Arabidopsis" "Oryza"       "Solanum"

``` r
mean(heights)
```

    ## [1] 11.9

``` r
median(heights)
```

    ## [1] 11.5

``` r
min(heights)
```

    ## [1] 9.8

``` r
max(heights)
```

    ## [1] 15.7

``` r
sum(heights)
```

    ## [1] 59.5

``` r
length(heights)
```

    ## [1] 5

``` r
treatments <- factor(c("Control", "Treatment A", "Treatment B", "Control", "Treatment A"))
treatments
```

    ## [1] Control     Treatment A Treatment B Control     Treatment A
    ## Levels: Control Treatment A Treatment B

``` r
treatments_2 <-c("Control", "Treatment A", "Treatment B", "Control", "Treatment A")
```

``` r
levels(treatments)
```

    ## [1] "Control"     "Treatment A" "Treatment B"

``` r
table(treatments)
```

    ## treatments
    ##     Control Treatment A Treatment B 
    ##           2           2           1

``` r
# สร้างข้อมูลใน column ต่างๆ "ชื่อcolumn" = c(...ข้อมูล...)
experiment <- data.frame(
  Plant_ID = 1:5, #1:5 คือ c(1,2,3,4,5)
  Species = c("Arabidopsis", "Arabidopsis", "Nicotiana", "Nicotiana", "Oryza"),
  Treatment = c("Control", "Drought", "Control", "Drought", "Control"),
  Height = c(10.2, 8.7, 15.3, 12.8, 25.4),
  Leaf_Count = c(8, 6, 12, 9, 7)
)

# View the data frame
experiment
```

    ##   Plant_ID     Species Treatment Height Leaf_Count
    ## 1        1 Arabidopsis   Control   10.2          8
    ## 2        2 Arabidopsis   Drought    8.7          6
    ## 3        3   Nicotiana   Control   15.3         12
    ## 4        4   Nicotiana   Drought   12.8          9
    ## 5        5       Oryza   Control   25.4          7

``` r
# สร้างข้อมูลใน column ต่างๆ "ชื่อcolumn" = c(...ข้อ
Plant_ID = c(1,2,3,4,5)
Species = c("Arabidopsis", "Arabidopsis", "Nicotiana", "Nicotiana", "Oryza")
Treatment = c("Control", "Drought", "Control", "Drought", "Control")
Height = c(10.2, 8.7, 15.3, 12.8, 25.4)
Leaf_Count = c(8, 6, 12, 9, 7)
#สร้างตาราง
experiment <-data.frame (Plant_ID,Species,Treatment,Height,Leaf_Count)
#ดูตาราง
experiment
```

    ##   Plant_ID     Species Treatment Height Leaf_Count
    ## 1        1 Arabidopsis   Control   10.2          8
    ## 2        2 Arabidopsis   Drought    8.7          6
    ## 3        3   Nicotiana   Control   15.3         12
    ## 4        4   Nicotiana   Drought   12.8          9
    ## 5        5       Oryza   Control   25.4          7

``` r
experiment$Treatment[2:4]
```

    ## [1] "Drought" "Control" "Drought"

``` r
tmp<-experiment$Plant_ID
tmp
```

    ## [1] 1 2 3 4 5

``` r
tmp = tmp+5
tmp
```

    ## [1]  6  7  8  9 10

``` r
experiment$Plant_ID<-tmp
experiment
```

    ##   Plant_ID     Species Treatment Height Leaf_Count
    ## 1        6 Arabidopsis   Control   10.2          8
    ## 2        7 Arabidopsis   Drought    8.7          6
    ## 3        8   Nicotiana   Control   15.3         12
    ## 4        9   Nicotiana   Drought   12.8          9
    ## 5       10       Oryza   Control   25.4          7

``` r
experiment$Plant_ID<-c(1,2,3,4,5)
experiment
```

    ##   Plant_ID     Species Treatment Height Leaf_Count
    ## 1        1 Arabidopsis   Control   10.2          8
    ## 2        2 Arabidopsis   Drought    8.7          6
    ## 3        3   Nicotiana   Control   15.3         12
    ## 4        4   Nicotiana   Drought   12.8          9
    ## 5        5       Oryza   Control   25.4          7

# การsubset ตาราง เอาแค่ข้อมูลบางแถว

``` r
#exp[..แถว..,..column..]
experiment[c(1,5),1:3] #โชว์ข้อมูลในแถว1และ5 ในcolumn 1ถึง3
```

    ##   Plant_ID     Species Treatment
    ## 1        1 Arabidopsis   Control
    ## 5        5       Oryza   Control

``` r
experiment[,1:3] #โชว์ข้อมูลทุกแถว ในcolumn 1ถึง3
```

    ##   Plant_ID     Species Treatment
    ## 1        1 Arabidopsis   Control
    ## 2        2 Arabidopsis   Drought
    ## 3        3   Nicotiana   Control
    ## 4        4   Nicotiana   Drought
    ## 5        5       Oryza   Control

``` r
experiment[c(1,5),] #โชว์ข้อมูลในแถว1และ5 ในทุก column
```

    ##   Plant_ID     Species Treatment Height Leaf_Count
    ## 1        1 Arabidopsis   Control   10.2          8
    ## 5        5       Oryza   Control   25.4          7

``` r
summary(experiment)
```

    ##     Plant_ID   Species           Treatment             Height     
    ##  Min.   :1   Length:5           Length:5           Min.   : 8.70  
    ##  1st Qu.:2   Class :character   Class :character   1st Qu.:10.20  
    ##  Median :3   Mode  :character   Mode  :character   Median :12.80  
    ##  Mean   :3                                         Mean   :14.48  
    ##  3rd Qu.:4                                         3rd Qu.:15.30  
    ##  Max.   :5                                         Max.   :25.40  
    ##    Leaf_Count  
    ##  Min.   : 6.0  
    ##  1st Qu.: 7.0  
    ##  Median : 8.0  
    ##  Mean   : 8.4  
    ##  3rd Qu.: 9.0  
    ##  Max.   :12.0

``` r
experiment[1:3, c("Species", "Height")]  # Rows 1-3, columns "Species" and "Height"
```

    ##       Species Height
    ## 1 Arabidopsis   10.2
    ## 2 Arabidopsis    8.7
    ## 3   Nicotiana   15.3

``` r
# Create a list containing different types of data
plant_data <- list(
  id = "AT001",
  species = "Arabidopsis thaliana",
  heights = c(10.2, 11.5, 9.8),
  is_model_organism = TRUE,
  germination_rates = data.frame(
    temperature = c(20, 25, 30),
    rate = c(0.82, 0.95, 0.78)
  )
)

# Access list elements
plant_data
```

    ## $id
    ## [1] "AT001"
    ## 
    ## $species
    ## [1] "Arabidopsis thaliana"
    ## 
    ## $heights
    ## [1] 10.2 11.5  9.8
    ## 
    ## $is_model_organism
    ## [1] TRUE
    ## 
    ## $germination_rates
    ##   temperature rate
    ## 1          20 0.82
    ## 2          25 0.95
    ## 3          30 0.78

``` r
plant_data$germination_rates$temperature
```

    ## [1] 20 25 30

\#Scatter Plots

``` r
# Create some data
plant_age <- c(5, 10, 15, 20, 25, 30) #vector data
plant_size <- c(3.2, 8.5, 13.7, 18.2, 21.5, 24.8) #vector data

# Create a basic scatter plot
plot(plant_age, plant_size, #plot (ชื่อแกนX,ชื่อแกนY)เอาชื่อมาจาก vector data ด้านบน
     main = "Plant Growth Over Time", #ช่ือกราฟ
     xlab = "Age (days)", #ชื่อแกน X
     ylab = "Height (cm)", #ชื่อแกน y
     col = "darkgreen", #สีจุด
     pch = 16)  # pch controls the point shape
```

![](basic1_files/figure-gfm/unnamed-chunk-27-1.png)<!-- -->

\#สร้างplotจากข้อมูล experiment

``` r
plot (experiment$Height , experiment$Leaf_Count,
     main = "Plant Growth", #ช่ือกราฟ
     xlab = "Age (days)", #ชื่อแกน X
     ylab = "Height (cm)", #ชื่อแกน y
     col = "hotpink", #สีจุด
     pch = 16)  # pch controls the point shape
```

![](basic1_files/figure-gfm/unnamed-chunk-28-1.png)<!-- -->

``` r
barplot(experiment$Leaf_Count,names.arg = experiment$Species,
        main = "wow",
        xlab = "species",
        ylab = "count",
        col = "pink",
        border = "black")
```

![](basic1_files/figure-gfm/unnamed-chunk-29-1.png)<!-- -->

``` r
tmp<-table(experiment$Species)
tmp
```

    ## 
    ## Arabidopsis   Nicotiana       Oryza 
    ##           2           2           1

``` r
names(tmp)
```

    ## [1] "Arabidopsis" "Nicotiana"   "Oryza"

``` r
barplot(tmp,
        name = names(tmp),
        main = "number of species",
        xlab = "species",
        ylab = "count",
        col = "pink",
        border = "black")
```

![](basic1_files/figure-gfm/unnamed-chunk-31-1.png)<!-- -->

``` r
# Create some data
treatment_A <- c(12.3, 14.5, 13.8, 15.2, 11.9, 13.7)
treatment_B <- c(15.8, 16.2, 14.9, 17.3, 16.5, 15.9)
treatment_C <- c(10.2, 11.5, 9.8, 10.5, 12.1, 11.3)

# Combine data for boxplot
all_data <- list(
  "Control" = treatment_A,
  "Fertilizer" = treatment_B,
  "Drought" = treatment_C
)

dat2<-data.frame(Control = treatment_A,
           Fertilizer = treatment_B,
           Drought = treatment_C)

# Create a boxplot
boxplot(all_data,
        main = "Plant Heights by Treatment",
        ylab = "Height (cm)",
        col = c("lightblue", "lightgreen", "salmon"))
```

![](basic1_files/figure-gfm/unnamed-chunk-32-1.png)<!-- -->

``` r
dat2 
```

    ##   Control Fertilizer Drought
    ## 1    12.3       15.8    10.2
    ## 2    14.5       16.2    11.5
    ## 3    13.8       14.9     9.8
    ## 4    15.2       17.3    10.5
    ## 5    11.9       16.5    12.1
    ## 6    13.7       15.9    11.3

``` r
# Perform a t-test
t_test_result <- t.test(dat2$Fertilizer, dat2$Control)

# View the result
t_test_result
```

    ## 
    ##  Welch Two Sample t-test
    ## 
    ## data:  dat2$Fertilizer and dat2$Control
    ## t = 4.1511, df = 8.4347, p-value = 0.002855
    ## alternative hypothesis: true difference in means is not equal to 0
    ## 95 percent confidence interval:
    ##  1.138545 3.928121
    ## sample estimates:
    ## mean of x mean of y 
    ##  16.10000  13.56667

``` r
dat2
```

    ##   Control Fertilizer Drought
    ## 1    12.3       15.8    10.2
    ## 2    14.5       16.2    11.5
    ## 3    13.8       14.9     9.8
    ## 4    15.2       17.3    10.5
    ## 5    11.9       16.5    12.1
    ## 6    13.7       15.9    11.3

``` r
plant_growth <- data.frame(
  Height = c(dat2$Control, dat2$Fertilizer, dat2$Drought),
  Treatment = factor(rep(c("Control", "Fertilizer", "Drought"), each = 6))
)
plant_growth
```

    ##    Height  Treatment
    ## 1    12.3    Control
    ## 2    14.5    Control
    ## 3    13.8    Control
    ## 4    15.2    Control
    ## 5    11.9    Control
    ## 6    13.7    Control
    ## 7    15.8 Fertilizer
    ## 8    16.2 Fertilizer
    ## 9    14.9 Fertilizer
    ## 10   17.3 Fertilizer
    ## 11   16.5 Fertilizer
    ## 12   15.9 Fertilizer
    ## 13   10.2    Drought
    ## 14   11.5    Drought
    ## 15    9.8    Drought
    ## 16   10.5    Drought
    ## 17   12.1    Drought
    ## 18   11.3    Drought

``` r
plant_growth$Treatment
```

    ##  [1] Control    Control    Control    Control    Control    Control   
    ##  [7] Fertilizer Fertilizer Fertilizer Fertilizer Fertilizer Fertilizer
    ## [13] Drought    Drought    Drought    Drought    Drought    Drought   
    ## Levels: Control Drought Fertilizer

``` r
# Perform one-way ANOVA
anova_result <- aov(Height ~ Treatment, data = plant_growth)
# Summary of the ANOVA results
summary(anova_result)
```

    ##             Df Sum Sq Mean Sq F value   Pr(>F)    
    ## Treatment    2  81.14   40.57   40.59 8.87e-07 ***
    ## Residuals   15  14.99    1.00                     
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
