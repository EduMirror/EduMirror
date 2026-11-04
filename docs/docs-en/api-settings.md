# API Settings

API settings configure the text models, image generation, and video generation services used by the platform. These settings affect simulation analysis, Rater evaluation, prompt generation, and media generation.

If a working default service is available, you normally do not need to change these settings. Configure a personal service when required by the platform administrator or your service provider.

The screenshot shows the text-model tab. Use the tabs at the top to view image and video settings.

```{image} _static/screenshots/05-api-settings.png
:alt: API settings: text-model configuration
:width: 40%
:align: center
```

## Service types

| Type | Purpose |
| --- | --- |
| Text model | Agent dialogue and decisions, scenario analysis, Rater evaluation, and prompt generation. |
| Image generation | Scenario comics and other images generated from simulation results. |
| Video generation | Presentation videos generated from simulation results. |

Each tab has its own service configuration.

## Text-model configuration

Typical fields include:

- **Provider**: the API service provider.
- **API Key**: leave this blank when using the platform's default simulation service; enter a provider-issued key when using your own service.
- **Base URL**: the provider's API endpoint, such as an OpenAI-compatible endpoint.
- **Model name**: the exact model identifier supported by the provider.

An incorrect Base URL or model name can cause both connection tests and simulations to fail.

## Image and video configuration

Open the image-generation or video-generation tab to configure its service. Typical fields include provider, API key, Base URL, and model or service name; use the fields displayed on the current page.

Image settings support comics and other visual content. Video settings support videos based on simulation events. After saving the configuration, submit the corresponding generation task from the media page.

## Testing and saving

1. Test the connection to check that the service is reachable and the model is recognized.
2. After a successful test, save the configuration to apply it.
3. Return to the simulation or media page and check the relevant function.

Use the delete-configuration control if you no longer need a configuration, then select another available one.

## Troubleshooting

### Connection test fails

Check that the API key is valid and unexpired, the Base URL is complete, the model name matches the provider's identifier, the provider account has sufficient quota, and the service is reachable from your network.

### Default service and usage limits

EduMirror provides a default simulation service that can be used without obtaining or entering an API key. Sign in to access the simulation functions supported by that service.

The default service may have daily run limits, concurrency limits, or other resource restrictions. Check the remaining run count in the account area and any messages displayed before a run. Current limits are determined by the platform.

To use a personal model service, enter and save its API key, Base URL, and model name. Availability also depends on the provider's permissions, quota, and network access.
