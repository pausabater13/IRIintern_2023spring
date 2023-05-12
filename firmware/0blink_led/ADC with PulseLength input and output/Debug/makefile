################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := ADC with PulseLength input and output
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
ADC\ with\ PulseLength\ input\ and\ output.elf \

MAP_FILES += \
ADC\ with\ PulseLength\ input\ and\ output.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
ADC\ with\ PulseLength\ input\ and\ output.list \


# All Target
all: main-build

# Main-build Target
main-build: ADC\ with\ PulseLength\ input\ and\ output.elf secondary-outputs

# Tool invocations
ADC\ with\ PulseLength\ input\ and\ output.elf ADC\ with\ PulseLength\ input\ and\ output.map: $(OBJS) $(USER_OBJS) /home/psabater/THRUST/thrust_controller-main/firmware/ADC\ with\ PulseLength\ input\ and\ output/STM32L011F4PX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "ADC with PulseLength input and output.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0plus -T"/home/psabater/THRUST/thrust_controller-main/firmware/ADC with PulseLength input and output/STM32L011F4PX_FLASH.ld" --specs=nosys.specs -Wl,-Map="ADC with PulseLength input and output.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

ADC\ with\ PulseLength\ input\ and\ output.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "ADC with PulseLength input and output.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) ADC\ with\ PulseLength\ input\ and\ output.elf ADC\ with\ PulseLength\ input\ and\ output.list ADC\ with\ PulseLength\ input\ and\ output.map ADC\\ with\\ PulseLength\\ input\\ and\\ output.elf default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
